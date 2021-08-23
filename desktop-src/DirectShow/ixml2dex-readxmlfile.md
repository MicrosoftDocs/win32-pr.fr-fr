---
description: La méthode ReadXMLFile charge un fichier de projet XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex :: ReadXMLFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 37df0c93a17dadc2f6d6fbf94a662b89bf9630a0b0861f5bf5a0c676f7d369fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952438"
---
# <a name="ixml2dexreadxmlfile-method"></a>IXml2Dex :: ReadXMLFile, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `ReadXMLFile` méthode charge un fichier projet XML. Cette méthode crée des instances de tous les objets exprimés dans le fichier XML et les insère dans la chronologie, ainsi que l’application de tous les attributs fournis pour la chronologie, tels que la fréquence d’images ou l’effet par défaut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimeline* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** d’un objet Timeline.

</dd> <dt>

*XMLName* 
</dt> <dd>

Chaîne qui spécifie le nom du fichier à charger.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur HRESULT. Les valeurs possibles sont les suivantes.



| Code de retour                                                                                                  | Description                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Succès<br/>             |
| <dl> <dt>**VFW \_ E \_ \_ format de fichier non valide \_**</dt> </dl> | Format de fichier non valide<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode n’efface pas les objets existants de la chronologie avant d’insérer les nouveaux objets définis dans le fichier XML. Si vous devez actualiser une chronologie existante, appelez d’abord [**IAMTimeline :: ClearAllGroups**](iamtimeline-clearallgroups.md) .

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

 

 




