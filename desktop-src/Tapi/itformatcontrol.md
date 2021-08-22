---
description: L’interface ITFormatControl expose des méthodes qui permettent à une application de récupérer des informations concernant le format d’un flux de réception ou de transmission pour un appel.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interface ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab42a9cacdf7986a652fff4e15195fec5f6b1aa319f06b631ee992541db40b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406049"
---
# <a name="itformatcontrol-interface"></a>Interface ITFormatControl

\[cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITFormatControl** expose des méthodes qui permettent à une application de récupérer des informations concernant le format d’un flux de réception ou de transmission pour un appel.

Cette interface est implémentée par le [MSP H323](h323-msp.md) et est exposée uniquement lorsqu’un appel utilise ce fournisseur de services.

## <a name="members"></a>Membres

L’interface **ITFormatControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITFormatControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITFormatControl** possède ces méthodes.



| Méthode                                                                     | Description                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Obtient le format multimédia du flux actuel.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Obtient le nombre de fonctionnalités associées au format actuel.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Obtient les fonctionnalités associées à un index de format donné.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Libère la structure associée au format.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Définit une nouvelle commande pour les fonctionnalités de format.<br/>                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

