---
title: Prototypes
description: Prototypes
ms.assetid: 2b31c01b-d52b-4df5-9cb0-a35286febd3a
keywords:
- Text Services Framework (TSF), prototypes
- TSF (Text Services Framework), prototypes
- Référence TSF, prototypes
- référence pour TSF, prototypes
- services de texte, prototypes
- Applications compatibles TSF, prototypes
- prototypes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417ea7a87e989cd66ae98ecaeae552699a7cead592278a3f156638dac769b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951648"
---
# <a name="prototypes"></a>Prototypes

[ITfContextRenderingMarkup](/windows/desktop/TSF/itfcontextrenderingmarkup), [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup)et [tf \_ RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) décrits dans cette référence ne sont pas définis dans des fichiers IDL ou d’en-tête. Les prototypes suivants doivent être respectés par le compilateur MIDL pour recevoir le fichier d’en-tête.


```C++
typedef struct
{
    ITfRange *pRange;
    TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;

// 
// IEnumTfRenderingMarkup 
// 
[
  object,
  uuid(8c03d21b-95a7-4ba0-ae1b-7fce12a72930),
  pointer_default(unique)
]
interface IEnumTfRenderingMarkup : IUnknown
{
    HRESULT Clone([out] IEnumTfRenderingMarkup **ppClone);

    HRESULT Next([in] ULONG ulCount,
                 [out, size_is(ulCount), length_is(*pcFetched)] TF_RENDERINGMARKUP *rgMarkup,
                 [out] ULONG *pcFetched);

    HRESULT Reset();

    HRESULT Skip([in] ULONG ulCount);
};

// 
// ITfContextRenderingMarkup 
// 
[
  object,
  uuid(a305b1c0-c776-4523-bda0-7c5a2e0fef10),
  pointer_default(unique)
]
interface ITfContextRenderingMarkup : IUnknown
{
    const DWORD TF_GRM_INCLUDE_PROPERTY = 0x1;

    HRESULT GetRenderingMarkup([in] TfEditCookie ec,
                               [in] DWORD dwFlags,
                               [in] ITfRange *pRangeCover,
                               [out] IEnumTfRenderingMarkup **ppEnum);
                                                           
    HRESULT FindNextRenderingMarkup([in] TfEditCookie ec,
                                    [in] DWORD dwFlags,
                                    [in] ITfRange *pRangeQuery,
                                    [in] TfAnchor tfAnchorQuery,
                                    [out] ITfRange **ppRangeFound,
                                    [out] TF_RENDERINGMARKUP *ptfRenderingMarkup);
};
```



 

 