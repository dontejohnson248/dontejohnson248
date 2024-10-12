# dontejohnson764


import React, { useState } from 'react';
2
3import Tilt from 'index';
4
5import './FlipPage.demozap.css';
6import { Page } from './Page/Page';
7
8const FlipPage = () => {
9  const [[flipVertically, flipHorizontally], toggleFlip] = useState([false, false]);
10
11  return (
12    <div className="flip-page">
13      <Tilt flipVertically={flipVertically} flipHorizontally={flipHorizontally}>
14        <Page
15          flipVertically={flipVertically}
16          flipHorizontally={flipHorizontally}
17          toggleFlipVertically={(checked) => toggleFlip([checked, flipHorizontally])}
18          toggleFlipHorizontally={(checked) => toggleFlip([flipVertically, checked])}
19        />
20      </Tilt>
21    </div>
22  );
23};
24
25export default FlipPage;
