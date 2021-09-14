---
title: Serveur de stratégie réseau
description: Le serveur NPS (Network Policy Server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS (Remote Authentication Dial-in User Service).
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011514"
---
# <a name="network-policy-server"></a>Serveur de stratégie réseau

## <a name="purpose"></a>Objectif

Le serveur NPS (Network Policy Server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS (Remote Authentication Dial-in User Service). Il s’agit du successeur du service d’authentification Internet (IAS).

En tant que serveur RADIUS, NPS effectue l’authentification, l’autorisation et la gestion des comptes pour les connexions sans fil, de commutateur d’authentification et d’accès à distance et de réseau privé virtuel (VPN).

NPS est également un serveur d’évaluateur d’intégrité pour la protection d’accès réseau (NAP). NPS effectue l’authentification et l’autorisation des tentatives de connexion réseau et, en fonction des stratégies de contrôle d’intégrité du système configurées, évalue la conformité de l’intégrité de l’ordinateur et détermine comment limiter l’accès réseau ou la communication d’un ordinateur non conforme. Il s’agit d’une nouvelle fonctionnalité spécifique à NPS uniquement. IAS ne la prend pas en charge. Consultez [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) pour obtenir une liste complète des fonctionnalités nouvelles sur NPS.

NPS comprend deux ensembles d’API : l’API d’extensions NPS et l’API d’objets de données serveur (SDO). L’API des extensions NPS et l’API SDO sont également prises en charge par le précurseur du serveur NPS, le service d’authentification Internet.

L’API extensions NPS peut être utilisée pour étendre les méthodes d’authentification, d’autorisation et de gestion des comptes offertes par NPS et précédemment par IAS.

L’API des objets de données du serveur peut être utilisée pour manipuler la configuration de la stratégie réseau sur un ordinateur exécutant NPS ou IAS.

> [!Note]  
> Les stratégies réseau dans NPS sont équivalentes aux stratégies d’accès à distance dans IAS.

 

## <a name="developer-audience"></a>Développeurs concernés

L’API extensions NPS est conçue pour être utilisée par les programmeurs qui utilisent le logiciel de développement C/C++. Les programmeurs doivent être familiarisés avec les concepts de mise en réseau et le protocole RADIUS. RADIUS est documenté dans le document [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) et [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

l’API Server Data objects est conçue pour être utilisée par les programmeurs à l’aide du logiciel de développement C/C++ ou Visual Basic. Les programmeurs doivent être familiarisés avec le [service d’accès à distance](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) et le protocole RADIUS.

## <a name="run-time-requirements"></a>Conditions d’exécution

l’API des Extensions NPS est prise en charge sur Windows Server 2008 avec l’installation du Service Microsoft Commercial Internet (MCIS).

l’API des objets de données du serveur est prise en charge sur Windows Server 2008.

NPS est disponible sur le serveur Windows 2008 avec l’installation du Service Microsoft Commercial Internet (MCIS).

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Vue d'ensemble](about-network-policy-server.md)
</dt> <dd>

Informations générales concernant RADIUS, IAS et NPS.

</dd> <dt>

[API des extensions du serveur NPS (Network Policy Server)](ias-extensions.md)
</dt> <dd>

API d’implémentation des dll d’extension utilisées pour l’authentification, l’autorisation et la gestion des comptes.

</dd> <dt>

[API des objets de données du serveur](server-data-objects.md)
</dt> <dd>

API pour la gestion de la configuration de la stratégie réseau.

</dd> <dt>

[SQL Programmabilité](sql-programmability.md)
</dt> <dd>

Exemples de procédures stockées utilisées pour la gestion de la journalisation NPS (IAS).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TechNet : serveur NPS (Network Policy Server)](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet : service d’authentification Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Protection d’accès réseau (NAP)](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 