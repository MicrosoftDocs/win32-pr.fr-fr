---
title: Init, méthode-CPapFile
description: L’exemple de code suivant montre comment CPapFile est initialisé.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- Init, méthode-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382432"
---
# <a name="init-method---cpapfile"></a>Init, méthode-CPapFile

L’exemple de code suivant montre comment **CPapFile** est initialisé.

Cet exemple est la méthode **CPapFile** **init** de Papfile. cpp.


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



Le paramètre *pszAppFileName* est utilisé pour initialiser CPapFile avec un nom de fichier par défaut pour toutes les opérations de chargement ou d’enregistrement ultérieures. Une copie est conservée dans le membre **m \_ szCurFileName** pour le premier chargement. Dans **StoClien**, une telle charge est tentée lorsque l’application démarre pour la première fois après que CPapFile a été initialisé avec *pszAppFileName* assignée à StoClien. PAP». Ce nom de fichier a été construit dans un constructeur CGuiPaper en obtenant le nom du module en cours d’exécution. (La fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) Win32 est appelée).

Le paramètre *pIPaper* est requis par CPapFile, car il utilise cette interface sur l’objet du copapier pour effectuer ses opérations de chargement et d’enregistrement. **AddRef** est appelé sur cette copie stockée de *pIPaper*, conformément aux règles com. La **version** correspondante est appelée dans le destructeur CPapFile.

 

 