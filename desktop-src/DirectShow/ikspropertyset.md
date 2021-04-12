---
description: L’interface IKsPropertySet a été conçue à l’origine comme un moyen efficace de définir et de récupérer les propriétés de l’appareil sur les pilotes WDM, à l’aide de KSProxy pour traduire les appels de la méthode COM en mode utilisateur dans les jeux de propriétés en mode noyau utilisés par les pilotes de classe de streaming WDM. Cette interface est désormais également utilisée pour transmettre des informations strictement entre les composants logiciels. Dans certains cas, les composants logiciels doivent implémenter cette interface, ou l’interface IKsControl (documentée dans DirectShow DDK). Par exemple, si vous écrivez un décodeur logiciel MPEG-2 pour une utilisation avec le navigateur DVD, vous devez implémenter l’une de ces interfaces et prendre en charge les jeux de propriétés relatives aux DVD que le navigateur enverra au décodeur. Les codes confidentiels peuvent prendre en charge l’une de ces interfaces pour permettre à d’autres broches ou filtres de définir ou de récupérer leurs propriétés. Notez qu’une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h. Les deux interfaces ne sont pas compatibles. L’interface IKsControl, documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interface IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480769"
---
# <a name="ikspropertyset-interface"></a>Interface IKsPropertySet

L' `IKsPropertySet` interface a été conçue à l’origine comme un moyen efficace de définir et de récupérer les propriétés de l’appareil sur les pilotes WDM, à l’aide de KSProxy pour traduire les appels de la méthode com en mode utilisateur dans les jeux de propriétés en mode noyau utilisés par les pilotes de classe de streaming WDM. Cette interface est désormais également utilisée pour transmettre des informations strictement entre les composants logiciels.

Dans certains cas, les composants logiciels doivent implémenter cette interface, ou l’interface **IKsControl** (documentée dans DirectShow DDK). Par exemple, si vous écrivez un décodeur logiciel MPEG-2 pour une utilisation avec le [navigateur DVD](dvd-navigator-filter.md), vous devez implémenter l’une de ces interfaces et prendre en charge les jeux de propriétés relatives aux DVD que le navigateur enverra au décodeur. Les codes confidentiels peuvent prendre en charge l’une de ces interfaces pour permettre à d’autres broches ou filtres de définir ou de récupérer leurs propriétés.

> [!Note]  
> Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h. Les deux interfaces ne sont pas compatibles. L’interface **IKsControl** , documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.

 

## <a name="members"></a>Membres

L’interface **IKsPropertySet** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPropertySet** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IKsPropertySet** possède ces méthodes.



| Méthode                                                  | Description                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Télécharger**](ikspropertyset-get.md)                       | Récupère une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.<br/> |
| [**QuerySupported**](ikspropertyset-querysupported.md) | Détermine si un objet prend en charge un jeu de propriétés spécifié.<br/>           |
| [**Définissez**](ikspropertyset-set.md)                       | Définit une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.<br/>      |



 

## <a name="remarks"></a>Notes

Vous devez inclure KS. h avant ksproxy. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothèque<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 
