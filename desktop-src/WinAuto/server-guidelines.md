---
title: Instructions du serveur
description: Pour que Microsoft Active Accessibility fonctionne comme prévu, les serveurs doivent fournir des informations d’accessibilité aux clients.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614549"
---
# <a name="server-guidelines"></a>Instructions du serveur

Pour que Microsoft Active Accessibility fonctionne comme prévu, les serveurs doivent fournir des informations d’accessibilité aux clients.

Pour implémenter [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), les développeurs de serveurs doivent suivre ce processus de base.

1.  Créez des objets accessibles en implémentant les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour vos éléments d’interface utilisateur personnalisés et pour le client de votre application. veillez à fournir une interface double qui prend en charge à la fois **IAccessible** et [**IDispatch**](idispatch-interface.md) afin que les clients écrits dans Microsoft Visual Basic et divers langages de script puissent obtenir des informations sur les objets.
2.  Appelez [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour informer les clients des modifications apportées à vos éléments d’interface utilisateur personnalisés.
3.  Gérez [**WM \_ GETOBJECT**](wm-getobject.md) pour fournir l’accès à vos objets accessibles.

Pour obtenir des suggestions et des conseils sur la conception d’objets accessibles, consultez le [Guide du développeur pour les serveurs Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Dans cette section

-   [Comment les serveurs implémentent des ID enfants](how-servers-implement-child-ids.md)

 

 




