---
description: La méthode WriteXML traduit une chronologie en une chaîne XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex :: WriteXML, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a5285faad36f83dbab693c63a0c96ca2b1d2b6a25220bb601a9527aac9dc5ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051289"
---
# <a name="ixml2dexwritexml-method"></a>IXml2Dex :: WriteXML, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `WriteXML` méthode traduit une chronologie en une chaîne XML.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimeline* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** de l’objet Timeline.

</dd> <dt>

*pbstrXML* 
</dt> <dd>

Pointeur vers une variable de type BSTR qui reçoit la chaîne XML décrivant la chronologie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. Si la mémoire est insuffisante pour la conversion, retourne E \_ OUTOFMEMORY. Sinon, retourne un autre code d’erreur.

## <a name="remarks"></a>Remarques

La méthode alloue de la mémoire pour la chaîne. L’application doit appeler **SysFreeString** pour libérer la mémoire.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4,0 ou version ultérieure<br/>                                               |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




