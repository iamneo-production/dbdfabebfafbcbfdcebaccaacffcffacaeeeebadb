import React, { useState } from 'react';
import validUrl from 'valid-url';

function UrlValidator() {
  const [url, setUrl] = useState('');
  const [domain, setDomain] = useState('');
  const [path, setPath] = useState('');
  const [method, setMethod] = useState('GET');
  const [body, setBody] = useState('');
  const [isValid, setIsValid] = useState(true);

  const handleValidate = () => {
    // Construct the full URL
    const fullUrl = `${domain}${path}`;

    // Check if the full URL is valid
    setIsValid(validUrl.isUri(fullUrl));
  };

  return (
    <div>
      <label>Domain:</label>
      <input type="text" value={domain} onChange={(e) => setDomain(e.target.value)} />

      <label>Path:</label>
      <input type="text" value={path} onChange={(e) => setPath(e.target.value)} />

      <label>Method:</label>
      <select value={method} onChange={(e) => setMethod(e.target.value)}>
        <option value="GET">GET</option>
        <option value="POST">POST</option>
        <option value="PUT">PUT</option>
        <option value="DELETE">DELETE</option>
      </select>

      <label>Body:</label>
      <textarea value={body} onChange={(e) => setBody(e.target.value)} />

      <button onClick={handleValidate}>Validate</button>

      {!isValid && <p style={{ color: 'red' }}>Invalid URL</p>}
    </div>
  );
}

export default UrlValidator;