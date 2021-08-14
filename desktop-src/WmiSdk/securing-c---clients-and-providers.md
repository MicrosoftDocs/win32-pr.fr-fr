---
description: Les fournisseurs C++ et les applications clientes doivent effectuer la plupart des opérations pour maintenir la sécurité WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Sécurisation des clients et des fournisseurs C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4151440f9e85f7cd9e6590842ffd3d103242410b38f52287dba83ba3bb3faec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316158"
---
# <a name="securing-c-clients-and-providers"></a>Sécurisation des clients et des fournisseurs C++

Les fournisseurs C++ et les applications clientes doivent effectuer la plupart des opérations pour maintenir la sécurité WMI.

Les applications clientes doivent définir correctement l' [emprunt d’identité](setting-the-default-process-security-level-using-c-.md) DCOM et les niveaux [d’authentification](setting-authentication-in-wmi.md) lors de la connexion à WMI. Les rappels des [appels asynchrones](setting-security-on-an-asynchronous-call.md) présentent des risques de sécurité, les applications clientes doivent donc [effectuer des vérifications d’accès](performing-access-checks.md) pour s’assurer que le rappel provient d’une source approuvée. Les clients doivent sécuriser les [consommateurs d’événements temporaires et permanents](securing-wmi-events.md).

Un fournisseur peut [effectuer des contrôles d’accès](performing-access-checks.md) pour s’assurer que les ressources qu’il crée sont accessibles uniquement par les clients appropriés.

Les fournisseurs et les clients peuvent également définir la sécurité sur une connexion [proxy spécifique](setting-the-security-on-iwbemservices-and-other-proxies.md) . Les deux peuvent également activer [des privilèges](executing-privileged-operations.md). Un fournisseur d’événements doit s’assurer que le consommateur client dispose des privilèges nécessaires pour [recevoir un événement demandé](providing-events-securely.md).

Un client ou un fournisseur peut avoir besoin d’établir une connexion à distance qui requiert un service d’authentification différent, NTLM au lieu de Kerberos par exemple.

 

 



