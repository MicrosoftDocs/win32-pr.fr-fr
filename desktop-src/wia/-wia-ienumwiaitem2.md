---
description: Utilisé par les applications pour énumérer les objets IWiaItem2 dans le dossier actif de l’arborescence d’éléments.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interface IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517550"
---
# <a name="ienumwiaitem2-interface"></a>Interface IEnumWiaItem2

Utilisé par les applications pour énumérer les objets [**IWiaItem2**](-wia-iwiaitem2.md) dans le dossier actif de l’arborescence d’éléments.

## <a name="members"></a>Membres

L’interface **IEnumWiaItem2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumWiaItem2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumWiaItem2** possède ces méthodes.



| Méthode                                          | Description                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Répliqué**](-wia-ienumwiaitem2-clone.md)       | Crée une instance supplémentaire de l’interface **IEnumWiaItem2** et retourne un pointeur vers celui-ci. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Retourne le nombre d’éléments stockés par cet énumérateur. <br/>                                                          |
| [**Suivant**](-wia-ienumwiaitem2-next.md)         | Remplit un tableau de pointeurs vers des interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .<br/>                                       |
| [**Réinitialiser**](-wia-ienumwiaitem2-reset.md)       | Réinitialise la référence d’énumération au premier objet [**IWiaItem2**](-wia-iwiaitem2.md) . <br/>                          |
| [**Saut**](-wia-ienumwiaitem2-skip.md)         | Ignore le nombre spécifié d’éléments au cours d’une énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
