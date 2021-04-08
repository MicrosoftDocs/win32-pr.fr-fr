---
title: Considérations relatives à Unicode
description: La fonction de service WriteFmtUserTypeStg, utilisée dans la méthode IPaper Save, requiert des paramètres de chaîne Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840058"
---
# <a name="unicode-considerations"></a><span data-ttu-id="79940-103">Considérations relatives à Unicode</span><span class="sxs-lookup"><span data-stu-id="79940-103">Unicode Considerations</span></span>

<span data-ttu-id="79940-104">La fonction de service **WriteFmtUserTypeStg** , utilisée dans la méthode [**IPaper :: Save**](ipaper--save.md) , requiert des paramètres de chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="79940-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="79940-105">C’est le cas avec les appels de service COM/OLE qui prennent des paramètres de chaîne.</span><span class="sxs-lookup"><span data-stu-id="79940-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="79940-106">Lors de la compilation pour les chaînes ANSI, les paramètres Unicode attendus doivent être converties d’ANSI en Unicode.</span><span class="sxs-lookup"><span data-stu-id="79940-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="79940-107">Ce processus est réalisé à l’aide de certaines macros dans APPUTIL. h qui peuvent masquer les conversions.</span><span class="sxs-lookup"><span data-stu-id="79940-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="79940-108">Par exemple, consultez **WriteFmtUserTypeStg**.</span><span class="sxs-lookup"><span data-stu-id="79940-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="79940-109">L’appel suivant apparaît dans la méthode [**Save**](ipaper--save.md) .</span><span class="sxs-lookup"><span data-stu-id="79940-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="79940-110">Quand **StoServe** est compilé pour ANSI (et non pour Unicode), cet appel réduit en fait un appel à une fonction de substitution apputil interne.</span><span class="sxs-lookup"><span data-stu-id="79940-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="79940-111">Pour prendre cela en charge, le schéma de macro suivant est utilisé dans apputil. h, qui est un fichier inclus dans tout l’exemple de code. Fichiers CPP.</span><span class="sxs-lookup"><span data-stu-id="79940-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="79940-112">Le schéma utilise des fonctions d’appel de service de substitution.</span><span class="sxs-lookup"><span data-stu-id="79940-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="79940-113">Les versions ANSI des appels commencent par un \_ .</span><span class="sxs-lookup"><span data-stu-id="79940-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="79940-114">Ces fonctions ANSI de substitution sont implémentées dans apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="79940-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="79940-115">Ils sont utilisés lorsque l’exemple de code est compilé pour les chaînes ANSI (valeur par défaut dans les Makefiles).</span><span class="sxs-lookup"><span data-stu-id="79940-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="79940-116">Les fonctions de service que les substituts sont en place ne prennent en charge que les paramètres de chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="79940-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="79940-117">Cela force certaines conversions de chaînes d’ANSI en Unicode avant l’appel du service COM/OLE réel dans le substitut.</span><span class="sxs-lookup"><span data-stu-id="79940-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="79940-118">Par exemple, si UNICODE n’est pas défini lors de la compilation, tous les appels dans les exemples à la fonction de service **WriteFmtUserTypeStg** com sont en fait modifiés par les macros dans les appels à une \_ fonction WriteFmtUserTypeStg qui est implémentée dans apputil. Cotisations.</span><span class="sxs-lookup"><span data-stu-id="79940-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="79940-119">Cette fonction accepte le pointeur de chaîne ANSI d’entrée, le convertit en copie Unicode et passe cette copie Unicode comme paramètre de chaîne dans un appel à la fonction **WriteFmtUserTypeStg** réelle.</span><span class="sxs-lookup"><span data-stu-id="79940-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="79940-120">Voici un \_ WriteFmtUserTypeStg de apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="79940-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




