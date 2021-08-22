---
title: Protection des informations d’identification et applications tierces
description: Credential Guard ne permet pas aux fournisseurs SSP tiers de demander des hachages de mot de passe à l’autorité de sécurité locale.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706749"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Fournisseurs de support de sécurité tiers avec Credential Guard

Credential Guard ne permet pas aux fournisseurs SSP tiers de demander des hachages de mot de passe à l’autorité de sécurité locale. Toutefois, les fournisseurs SSP et les points d’accès reçoivent toujours des notifications du mot de passe lorsqu’un utilisateur se connecte et/ou modifie son mot de passe. Aucune utilisation d’API non documentées dans des fournisseurs SSP et des points d’accès personnalisés n’est prise en charge.

La profondeur et l’étendue des protections fournies par Credential Guard évoluant sans cesse, les versions ultérieures de Windows 10 avec Credential Guard peuvent affecter des scénarios qui fonctionnaient précédemment. Par exemple, Credential Guard peut bloquer l’utilisation d’un type particulier d’informations d’identification ou d’un composant particulier pour empêcher les programmes malveillants de tirer parti des vulnérabilités. Par conséquent, nous recommandons que les scénarios nécessaires aux opérations d’une organisation soient testés avant de mettre à niveau un appareil sur lequel Credential Guard est exécuté.

Reportez-vous à [cet article](/windows/security/identity-protection/credential-guard/credential-guard) pour obtenir la description complète et les atténuations recommandées.

 

 