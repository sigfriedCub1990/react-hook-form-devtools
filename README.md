<h1 align="center">React Hook Form Dev Tools</h1>
<p align="center"><b>🤹‍♀️ Under development</b></p>

<div align="center">
    <p align="center">
        <a href="https://react-hook-form.com" title="React Hook Form - Simple React forms validation">
            <img src="https://raw.githubusercontent.com/bluebill1049/react-hook-form/master/website/logo.png" alt="React Hook Form Logo - React hook custom hook for form validation" width="300px" />
        </a>
    </p>
</div>

<p align="center">Performant, flexible and extensible forms with easy to use validation.</p>

<div align="center">

[![npm downloads](https://img.shields.io/npm/dm/react-hook-form.svg?style=flat-square)](https://www.npmjs.com/package/react-hook-form)
[![npm](https://img.shields.io/npm/dt/react-hook-form.svg?style=flat-square)](https://www.npmjs.com/package/react-hook-form)
![dep](https://badgen.net/david/dep/bluebill1049/react-hook-form)
[![npm](https://badgen.net/bundlephobia/minzip/react-hook-form)](https://badgen.net/bundlephobia/minzip/react-hook-form)
[![Coverage Status](https://coveralls.io/repos/github/bluebill1049/react-hook-form/badge.svg?branch=master)](https://coveralls.io/github/bluebill1049/react-hook-form?branch=master)

[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=React+hooks+for+form+validation+without+the+hassle&url=https://github.com/bluebill1049/react-hook-form)&nbsp;[![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/react-hook-form)

</div>

<img src="https://raw.githubusercontent.com/react-hook-form/react-hook-form-devtools/master/app/screen.png" />

This React Component will help you to debug when you are working React Hook Form, and give you more insight about your form detail.

## Install

    $ npm install react-hook-form-devtools

## Quickstart

```typescript jsx
import React from 'react';
import { useForm } from 'react-hook-form';
import DevTool from './devlTool';
import './App.css';

const App = () => {
  const { register, control, handleSubmit } = useForm({
    mode: 'onChange',
  });

  return (
    <>
      <DevTool control={control} />

      <form onSubmit={handleSubmit(d => console.log(d))}>
        <h1>React Hook Form DevTools</h1>
        <label>Test</label>
        <input name="test" ref={register} />
        <input type="submit" />
      </form>
    </>
  );
};

export default App;
```
