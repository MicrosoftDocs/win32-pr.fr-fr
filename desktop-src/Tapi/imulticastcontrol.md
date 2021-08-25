---
description: L’interface IMulticastControl est implémentée par le MSP IPConf et disponible uniquement sur les objets d’appel de multidiffusion.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interface IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7469ca26a49bc25b36ae87727a1fdcf324bcf54e8a253805ed56f252c7f062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905949"
---
# <a name="imulticastcontrol-interface"></a>Interface IMulticastControl

\[**IMulticastControl** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IMulticastControl** est implémentée par le MSP ipconf et disponible uniquement sur les objets d’appel de multidiffusion. Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP. L’interface **IMulticastControl** contrôle le mode de bouclage de multidiffusion.

En mode de \_ \_ bouclage mm, la multidiffusion est désactivée, ce qui signifie que deux applications sur le même ordinateur qui rejoignent le même groupe de multidiffusion obtiendront les paquets de chacun d’eux. Ce mode offre les meilleures performances si une seule application est toujours jointe au groupe de multidiffusion sur l’ordinateur. MM \_ aucun \_ mode de bouclage n’est le mode par défaut.

Le \_ \_ mode de bouclage complet mm est parfait uniquement pour les tests. Tous les paquets envoyés sont également renvoyés en boucle. Cela peut être utilisé pour tester si les appareils fonctionnent.

Le \_ mode de \_ bouclage sélectif mm est utilisé pour permettre à plusieurs applications sur un ordinateur de rejoindre le même groupe de multidiffusion. Les paquets sont rebouclés de la pile et chaque session RTP est chargée de filtrer les paquets indésirables.

## <a name="members"></a>Membres

L’interface **IMulticastControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMulticastControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMulticastControl** possède ces méthodes.



| Méthode                                                          | Description                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**Obtient \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Obtient le mode de bouclage de multidiffusion.<br/> |
| [**put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Définit le mode de bouclage de multidiffusion.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> </dl>

 

