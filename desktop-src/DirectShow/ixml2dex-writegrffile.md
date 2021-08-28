---
description: La méthode WriteGrfFile écrit un graphique de filtre dans un fichier au format. GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex :: WriteGrfFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 121d901bee9da9b8ea6f7dad31e589002c0b4859619f6dd02941f438af3b647f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767019"
---
# <a name="ixml2dexwritegrffile-method"></a>IXml2Dex :: WriteGrfFile, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `WriteGrfFile` méthode écrit un graphique de filtre dans un fichier au format. GRF.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGraph* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** du graphique de filtre.

</dd> <dt>

*FileName* 
</dt> <dd>

Chaîne qui spécifie le nom du fichier à écrire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de l’interface. HRESULT peut inclure l’une des constantes standard suivantes, ou d’autres valeurs non listées.



| Code de retour                                                                                  | Description                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>       | Échec.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’argument n’est pas valide.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>             |



 

Cette méthode peut également retourner des codes d’erreur générés par des appels internes aux méthodes **IStorage :: CreateStream,** et **IPersist :: Save** . Pour plus d’informations, consultez le kit de développement Platform SDK.

## <a name="remarks"></a>Remarques

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

 

 




