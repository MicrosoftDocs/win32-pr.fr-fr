---
title: Proxy d'application web
description: Proxy d'application web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a346297dca0a81d8c2269b61e8a5d581f03f95fab56e044bedce7513882535f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211324"
---
# <a name="web-application-proxy"></a>Proxy d'application web

## <a name="platform"></a>Plateforme

**serveurs-** Windows Server 2012 R2  






## <a name="description"></a>Description

dans Windows Server 2012 R2, nous avons ajouté un nouveau service appelé Proxy d’Application Web sous le rôle accès à distance qui permet aux administrateurs de publier des applications pour un accès externe. Ce service agit comme un proxy inverse et comme un proxy services de fédération Active Directory (AD FS) (AD FS). En fait, ce service remplace le service de proxy AD FS tel qu’il a été connu dans Windows Server 2012.

Avec le proxy d’application Web, une organisation peut mettre des ressources Web locales à la disposition d’un accès externe tout en gérant le risque de cet accès en contrôlant les stratégies d’authentification et d’autorisation sur le AD FS.

## <a name="manifestation"></a>Manifestation

Le service proxy AD FS n’est plus sous le rôle services de fédération Active Directory (AD FS) (AD FS), mais il a été remplacé par le proxy d’application Web sous le rôle accès à distance. Cela représente une expansion du service de proxy AD FS en incluant la fonctionnalité de proxy inverse pour la publication d’applications.

## <a name="solution"></a>Solution

Pour accéder au proxy d’application Web, les administrateurs peuvent accéder à Gestionnaire de serveur et ajouter un nouveau rôle/service de rôle. L’administrateur trouvera le proxy d’application Web sous le rôle accès à distance.

## <a name="resources"></a>Ressources

-   [Guide des solutions](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 