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
# <a name="init-method---cpapfile"></a><span data-ttu-id="59960-104">Init, méthode-CPapFile</span><span class="sxs-lookup"><span data-stu-id="59960-104">Init Method - CPapFile</span></span>

<span data-ttu-id="59960-105">L’exemple de code suivant montre comment **CPapFile** est initialisé.</span><span class="sxs-lookup"><span data-stu-id="59960-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="59960-106">Cet exemple est la méthode **CPapFile** **init** de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="59960-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


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



<span data-ttu-id="59960-107">Le paramètre *pszAppFileName* est utilisé pour initialiser CPapFile avec un nom de fichier par défaut pour toutes les opérations de chargement ou d’enregistrement ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59960-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="59960-108">Une copie est conservée dans le membre **m \_ szCurFileName** pour le premier chargement.</span><span class="sxs-lookup"><span data-stu-id="59960-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="59960-109">Dans **StoClien**, une telle charge est tentée lorsque l’application démarre pour la première fois après que CPapFile a été initialisé avec *pszAppFileName* assignée à StoClien. PAP».</span><span class="sxs-lookup"><span data-stu-id="59960-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="59960-110">Ce nom de fichier a été construit dans un constructeur CGuiPaper en obtenant le nom du module en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="59960-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="59960-111">(La fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) Win32 est appelée).</span><span class="sxs-lookup"><span data-stu-id="59960-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="59960-112">Le paramètre *pIPaper* est requis par CPapFile, car il utilise cette interface sur l’objet du copapier pour effectuer ses opérations de chargement et d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="59960-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="59960-113">**AddRef** est appelé sur cette copie stockée de *pIPaper*, conformément aux règles com.</span><span class="sxs-lookup"><span data-stu-id="59960-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="59960-114">La **version** correspondante est appelée dans le destructeur CPapFile.</span><span class="sxs-lookup"><span data-stu-id="59960-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 