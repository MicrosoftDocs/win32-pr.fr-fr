---
description: Le DDE réseau utilise des partages approuvés et des descripteurs de sécurité pour contrôler l’accès aux partages.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Partages et sécurité approuvés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bed3b520597f6cabe95929d2ee5bf9c29af6bb6c524d2aa136f4c86392cbb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014679"
---
# <a name="trusted-shares-and-security"></a>Partages et sécurité approuvés

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Le DDE réseau utilise des partages approuvés et des descripteurs de sécurité pour contrôler l’accès aux partages.

## <a name="trusted-shares"></a>Partages approuvés

Lorsqu’un utilisateur client se connecte à un partage DDE à partir d’un ordinateur distant, DDE réseau accepte la demande uniquement si les instructions suivantes sont vraies :

-   L’utilisateur qui a créé le partage a accordé un État approuvé au partage en appelant [**NDdeSetTrustedShare**](nddesettrustedshare.md). Seul le créateur du partage peut accorder un État approuvé au partage. Aucun administrateur ne peut accorder l’État approuvé à un partage DDE créé par un autre utilisateur.
-   L’utilisateur qui a créé le partage est actuellement connecté à l’ordinateur serveur.

Le processus d’octroi de l’État approuvé à un partage ajoute le partage à la liste des partages approuvés de l’utilisateur connecté dans le DSDM. Cela crée une relation d’approbation entre le serveur et ses clients. Une fois qu’un partage DDE a l’État approuvé, les clients peuvent s’y connecter tant que l’utilisateur qui a créé le partage est connecté. Lorsque le client se connecte au partage à partir d’un ordinateur distant, DDE réseau accepte la demande uniquement si le partage est répertorié dans la liste des partages approuvés de l’utilisateur connecté dans le DSDM.

## <a name="security"></a>Sécurité

Le DDE réseau effectue une vérification de sécurité supplémentaire lorsque le client demande des données ou un lien. Il vérifie que le serveur a accordé à l’utilisateur distant l’autorisation nécessaire pour l’opération. Le serveur contrôle l’accès au partage via le paramètre *pSD* de la fonction [**NDdeShareAdd**](nddeshareadd.md) . Ce paramètre spécifie le descripteur de sécurité. Si ce paramètre a la **valeur null**, la fonction crée un descripteur de sécurité par défaut qui accorde un accès complet au créateur du partage et accorde une autorisation de lecture et de liaison à tous les autres utilisateurs. Pour accorder ou refuser des autorisations supplémentaires à des utilisateurs individuels ou à des groupes d’utilisateurs, créez et utilisez un descripteur de sécurité. Pour plus d’informations sur les descripteurs de sécurité, consultez [**Access Control**](/windows/desktop/SecAuthZ/access-control).

Pour obtenir le descripteur de sécurité d’un partage DDE existant, appelez la fonction [**NDdeGetShareSecurity**](nddegetsharesecurity.md) . Vous pouvez modifier les informations, puis mettre à jour le descripteur de sécurité du partage à l’aide de la fonction [**NDdeSetShareSecurity**](nddesetsharesecurity.md) .

 

 
