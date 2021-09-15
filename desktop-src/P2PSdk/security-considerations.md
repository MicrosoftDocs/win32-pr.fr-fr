---
description: Cette rubrique décrit des considérations de sécurité spécifiques lors de l’utilisation de l’infrastructure homologue.
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: Considérations relatives à la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413658"
---
# <a name="security-considerations"></a>Considérations relatives à la sécurité

Cette rubrique décrit des considérations de sécurité spécifiques lors de l’utilisation de l’infrastructure homologue.

Lorsque vous développez une application homologue à l’aide de l’infrastructure d’homologue, pour des raisons de sécurité, vous devez prendre en compte les autorisations d’annuaire, l’accès invité aux services réseau homologues, la divulgation d’informations et l’implémentation du fournisseur de services de sécurité

## <a name="directory-permissions"></a>Autorisations de répertoire

Les services de réseau pair à pair stockent des données dans l’arborescence de répertoires du profil utilisateur d’un utilisateur. Un utilisateur doit disposer d’autorisations en écriture dans la sous-arborescence des **données d’application** du profil. Par défaut, cette liste de contrôle d’accès (ACL) est définie correctement, mais un utilisateur peut la modifier manuellement.

## <a name="guest-access-to-peer-networking-services"></a>Accès invité aux services de réseau pair à pair

un compte invité et les membres du groupe Sécurité Windows **invités** n’ont pas accès à la plupart des services homologues. Les applications doivent disposer d’un accès utilisateur local ou supérieur.

## <a name="information-disclosure"></a>Information Disclosure (divulgation d’informations)

La divulgation d’informations implique l’adresse, la base de données et les informations d’identification du groupe et de l’identité. Les sections suivantes identifient et définissent la divulgation d’informations.

**Divulgation d’adresses** Le protocole PNRP (Peer Name Resolution Protocol) est un service de résolution d’identificateur qui permet à un identificateur de nom d’homologue d’être résolu en une adresse IP. Semblable à DNS, PNRP publie une adresse IP afin que les utilisateurs qui connaissent l’identificateur correspondant puissent le résoudre en cette adresse.

-   La publication d’un identificateur dans PNRP signifie que tout utilisateur peut résoudre l’identificateur vers l’adresse IP publiée et déterminer l’adresse IP du service PNRP qui a publié l’identité.
-   L’infrastructure de regroupement de pairs publie automatiquement le nom du groupe homologue de l’instance de groupe locale dans PNRP. Lorsque vous êtes connecté à un groupe homologue, toute personne connaissant le nom d’homologue du groupe peut résoudre les adresses des membres actifs et connaître l’adresse actuelle de chaque utilisateur.

La capacité d’un utilisateur à se connecter à d’autres membres du groupe homologue ou à des nœuds de graphique d’homologue lorsqu’il est connecté est une fonctionnalité principale du réseau pair à pair. Lorsque vous êtes connecté à un groupe pair ou à un graphique, l’adresse IP actuelle d’un utilisateur peut être publiée dans un enregistrement de présence au sein du groupe homologue ou du graphique. Par défaut, toute personne participant à ce groupe ou graphique pair peut énumérer les membres du groupe ou du graphique et déterminer les adresses actuelles des membres. Cette capacité est un regroupement configurable et une propriété de représentation graphique d’homologue.

**Divulgation de base de données** Les infrastructures de regroupement et de représentation graphique des pairs sont stockées sur le système de fichiers local. tout utilisateur Windows disposant d’un accès administratif au système de fichiers local (par exemple, un administrateur local) peut accéder en théorie aux données de la base de données du graphique ou du groupe d’homologues local. Cela est cohérent avec la possibilité pour les administrateurs locaux d’accéder à toutes les données sur l’ordinateur local.

**Divulgation des informations d’identification de groupe et d’identité** Le regroupement d’égal à égal exige que les membres établissent des connexions entre eux pour s’authentifier à l’aide de chaînes de certificats X. 509 modifiées. Dans le cadre de l’authentification, les chaînes d’identité et de certificat d’appartenance de groupe (GMC) correspondantes de chaque membre sont échangées.

Lors d’une connexion à un groupe homologue, l’infrastructure de regroupement d’homologues publie le nom d’homologue de groupe avec PNRP. Dans le cadre de l’opération PNRP normale, la chaîne GMC de ce groupe peut être fournie à d’autres instances PNRP pour prouver l’autorisation de publier le nom d’homologue du groupe.

## <a name="security-service-provider-implementation"></a>Implémentation du fournisseur de services de sécurité

L’infrastructure de représentation graphique des pairs est aussi sécurisée que le fournisseur de services de sécurité (SSP) que le développeur d’applications implémente. Plus le SSP est fort, plus la sécurité de l’application de représentation graphique des pairs est forte.

 

 



