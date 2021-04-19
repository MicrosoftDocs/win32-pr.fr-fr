---
description: La méthode WriteXMLFile convertit une chronologie en XML et écrit les données XML dans un fichier.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex :: WriteXMLFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533219"
---
# <a name="ixml2dexwritexmlfile-method"></a>IXml2Dex :: WriteXMLFile, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `WriteXMLFile` méthode convertit une chronologie en XML et écrit les données XML dans un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimeline* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** de l’objet Timeline.

</dd> <dt>

*FileName* 
</dt> <dd>

Chaîne qui spécifie le nom du fichier à écrire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de l’interface. Le **HRESULT** peut inclure l’une des constantes standard suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                   | Description                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L’argument n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>             |



 

## <a name="remarks"></a>Notes

Cette méthode génère un fichier XML qui représente tous les composants de la chronologie.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

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

 

 




