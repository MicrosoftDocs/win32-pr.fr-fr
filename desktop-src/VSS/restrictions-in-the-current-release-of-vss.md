---
description: 'certaines fonctionnalités prévues pour la version de Windows Server 2003 de VSS ne sont pas entièrement prises en charge :'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Restrictions dans Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7353b2d52a7222015f051e15ba07830b81d6aedda6323bca4378f459eb602ba8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124509"
---
# <a name="restrictions-in-windows-server-2003"></a>Restrictions dans Windows Server 2003

certaines fonctionnalités prévues pour la version de Windows Server 2003 de VSS ne sont pas entièrement prises en charge :

-   Pendant les opérations de sauvegarde, plusieurs instances d’une classe de writer donnée sont autorisées uniquement si une seule de ces instances a un état de restauration de l’enregistreur (consultez [**VSS \_ WRITERRESTORE \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) autre que VSS \_ WRE \_ jamais. Si cette condition est remplie, toutes les instances d’enregistreur participent pleinement au cours de la sauvegarde, générant des documents de métadonnées de l’enregistreur et participant à la gestion des événements.
-   Pendant les opérations de restauration, un seul enregistreur recevra les événements de restauration générés par le demandeur. Si plusieurs instances d’une classe Writer ont un État Restore de l’enregistreur défini sur une valeur autre que VSS \_ WRE \_ jamais, une seule instance recevra les événements Restore. L’instance qui les recevra est indéterminée.

 

 



