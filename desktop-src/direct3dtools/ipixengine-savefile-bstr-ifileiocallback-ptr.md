---
description: Enregistre le journal de graphisme à l’emplacement spécifié.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine :: SaveFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5414be69d114d7e6072e36eb6257e716241d02881aa2032063066bed99d243f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981089"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine :: SaveFile, méthode

Enregistre le journal de graphisme à l’emplacement spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a>Paramètres

*Extension*   
Chaîne COM contenant le nom du chemin d’accès du journal de graphisme enregistré.

*pFileIOCallback*   
Adresse d’un importation utilisé pour notifier l’hôte des erreurs d’e/s de fichier lors de l’enregistrement.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
