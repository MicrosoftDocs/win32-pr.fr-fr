---
title: Services de base du module de plateforme sécurisée
description: Le logiciel TPM fournit des services sous la forme d’une API exposée via un appel de procédure distante. Utilisez TPM pour créer un module TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- Services de base TPM TBS
- GPC base services TBS, page d’hébergement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ccec7d7e70d8dece377518b379c0597c1392a3266222d6e70fa3ac524a010f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880460"
---
# <a name="tpm-base-services"></a>Services de base du module de plateforme sécurisée

## <a name="purpose"></a>Objectif

La fonctionnalité des services de base de la Module de plateforme sécurisée (TPM) (TBS) centralise l’accès au module de plateforme sécurisée entre les applications.

La fonctionnalité TBS s’exécute en tant que service système dans Windows Server 2008, Windows Vista ou des systèmes d’exploitation plus récents. Il fournit des services comme une API exposée par le biais d’appels de procédure distante (RPC). La fonctionnalité TBS utilise des priorités spécifiées en appelant des applications pour planifier de manière coopérative l’accès au TPM.

> [!Note]
>
> Le module de plateforme sécurisée peut être utilisé pour les opérations de stockage de clés. Toutefois, les développeurs sont encouragés à utiliser les [API de stockage de clés](/windows/desktop/SecCNG/key-storage-and-retrieval) pour ces scénarios à la place. Les API de stockage de clé offrent les fonctionnalités permettant de créer, signer ou chiffrer des clés de chiffrement, ainsi que de les rendre persistantes. elles sont plus haut et plus faciles à utiliser que le TBS pour ces scénarios ciblés.

 

## <a name="developer-audience"></a>Développeurs concernés

TBS est destiné aux développeurs d’applications basées sur les systèmes d’exploitation Windows. Les développeurs doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation Microsoft Windows.

## <a name="run-time-requirements"></a>Conditions d’exécution

La fonctionnalité TBS requiert au moins le système d’exploitation Windows Server 2008 ou Windows Vista. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                         | Description                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [À propos de TBS](about-tbs.md)<br/>         | Concepts clés et une vue de haut niveau de la fonctionnalité TBS.<br/>               |
| [Utilisation de TBS](using-tbs.md)<br/>         | Processus et procédures TBS pour l’utilisation de l’API TBS.<br/>                  |
| [Référence TBS](tbs-reference.md)<br/> | Documentation sur les fonctions TBS, les structures et les codes de retour.<br/> |



 

 

