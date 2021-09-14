---
title: API de serveur HTTP
description: L’API du serveur HTTP permet aux applications de communiquer sur HTTP sans utiliser Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API de serveur HTTP
- API serveur HTTP, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234048"
---
# <a name="http-server-api"></a>API de serveur HTTP

## <a name="purpose"></a>Objectif

L’API du serveur HTTP permet aux applications de communiquer sur HTTP sans utiliser Microsoft Internet Information Server (IIS). Les applications peuvent s’inscrire pour recevoir des requêtes HTTP pour des URL particulières, recevoir des requêtes HTTP et envoyer des réponses HTTP. L’API du serveur HTTP comprend la prise en charge SSL afin que les applications puissent échanger des données via des connexions HTTP sécurisées sans IIS. Il est également conçu pour fonctionner avec des ports de terminaison d’e/s.

## <a name="developer-audience"></a>Développeurs concernés

Cette API est conçue pour être utilisée par les programmeurs C/C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

l’API du serveur HTTP est prise en charge sur les systèmes d’exploitation Windows server 2003 et sur Windows XP avec Service Pack 2 (SP2). n’oubliez pas que Microsoft IIS 5 s’exécutant sur Windows XP avec SP2 ne peut pas partager le port 80 avec d’autres applications HTTP exécutées simultanément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                           | Description                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [À propos de l’API du serveur HTTP](about-http-server-api.md)<br/>                   | Informations générales sur HTTP.<br/>                                                              |
| [Utilisation de l’API du serveur HTTP](using-http-server-api.md)<br/>                   | Guide de procédures pour l’utilisation de HTTP.<br/>                                                             |
| [Référence de l’API du serveur HTTP](http-server-api-reference.md)<br/>           | Documentation des fonctions, structures et types d’énumération spécifiques disponibles dans HTTP.<br/>    |
| [Exemple d’application de serveur HTTP](http-server-sample-application.md)<br/> | Exemple d’application qui montre comment utiliser l’API du serveur HTTP pour effectuer des tâches côté serveur.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Services HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

