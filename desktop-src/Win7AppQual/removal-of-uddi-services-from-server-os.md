---
description: Suppression des services UDDI du système d’exploitation serveur
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Suppression des services UDDI du système d’exploitation serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193060"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Suppression des services UDDI du système d’exploitation serveur

## <a name="affected-platform"></a>Plateforme affectée

**serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -faible  

## <a name="description"></a>Description

Microsoft a supprimé le rôle serveur Services UDDI (Universal Description, Discovery, and integration) de Windows server 2008 R2. Les versions ultérieures des services UDDI feront partie du produit Microsoft BizTalk. Cette réalignement et la consolidation des produits permettent à Microsoft de mieux servir le marché de l’architecture orientée services (SOA).

la première version 2008 du serveur de Windows publication des Services uddi sera conforme aux normes uddi v 3.0. elle est fournie dans le cadre de la version BizTalk Server 2009. pour répondre à notre engagement à fournir une expérience utilisateur satisfaisante, nous proposons un package d’installation des Services UDDI v3 pour Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestation

la présence de versions précédentes des composants des Services UDDI sur le système bloque une mise à niveau vers Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Atténuation de l’impact

les utilisateurs qui ont déployé un site de Services uddi à partir de Windows server 2003 ou Windows server 2008 peuvent choisir de ne pas mettre à niveau les serveurs qui exécutent les services uddi vers Windows Server 2008 R2. ils peuvent également déplacer les services uddi vers des zones dédiées Windows server 2003 ou Windows server 2008 s’ils doivent mettre à niveau les zones des services uddi actuelles.

## <a name="solution"></a>Solution

la solution recommandée consiste à déployer les Services UDDI v 3.0 à partir de BizTalk Server 2009 sur un ordinateur Windows Server 2008 R2, puis à migrer l’ancien site vers le nouveau site. Les services UDDI v 3.0 offrent une compatibilité descendante avec les services UDDI 2,0, si bien que toutes les applications qui utilisent des services UDDI ne seront pas affectées.

Pour ce faire, procédez comme suit :

1.  configurez un nouveau site UDDI Services v 3.0 sur un ordinateur déjà chargé avec Windows Server 2008 R2. (remarque : dans une installation distribuée, un site UDDI v 3.0 peut être constitué de plusieurs machines Windows Server 2008 R2).
2.  Utilisez l’outil de migration de données UDDI pour migrer les données de l’ancienne base de données des services UDDI vers la nouvelle base de données.
3.  Sauvegardez l’ancienne base de données des services UDDI pour garantir la restauration.
4.  désinstallez les anciens logiciels des Services UDDI, puis mettez-les à niveau vers Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Site Web des services Microsoft UDDI](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Spécifications UDDI](http://uddi.xml.org/specification)
-   [téléchargement des Services UDDI v 3.0 pour Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



