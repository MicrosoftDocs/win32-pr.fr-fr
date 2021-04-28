---
description: Suppression des services UDDI du système d’exploitation serveur
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Suppression des services UDDI du système d’exploitation serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116327"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Suppression des services UDDI du système d’exploitation serveur

## <a name="affected-platform"></a>Plateforme affectée

**Serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -faible  

## <a name="description"></a>Description

Microsoft a supprimé le rôle serveur services UDDI (Universal Description, Discovery, and Integration) de Windows Server 2008 R2. Les versions ultérieures des services UDDI feront partie du produit Microsoft BizTalk. Cette réalignement et la consolidation des produits permettent à Microsoft de mieux servir le marché de l’architecture orientée services (SOA).

La première version postérieure à Windows Server 2008 des services UDDI sera compatible avec les normes UDDI v 3.0. Elle est fournie dans le cadre de la version BizTalk Server 2009. Pour répondre à notre engagement à fournir une expérience utilisateur satisfaisante, nous proposons un package d’installation des services UDDI V3 pour Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestation

La présence de versions précédentes des composants des services UDDI sur le système bloque une mise à niveau vers Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Atténuation de l’impact

Les utilisateurs qui ont déployé un site de services UDDI à partir de Windows Server 2003 ou Windows Server 2008 peuvent choisir de ne pas mettre à niveau les serveurs qui exécutent les services UDDI vers Windows Server 2008 R2. Ils peuvent également déplacer les services UDDI vers des zones Windows Server 2003 ou Windows Server 2008 dédiées s’ils doivent mettre à niveau les zones des services UDDI en cours.

## <a name="solution"></a>Solution

La solution recommandée consiste à déployer les services UDDI v 3.0 à partir de BizTalk Server 2009 sur un ordinateur Windows Server 2008 R2, puis à migrer l’ancien site vers le nouveau site. Les services UDDI v 3.0 offrent une compatibilité descendante avec les services UDDI 2,0, si bien que toutes les applications qui utilisent des services UDDI ne seront pas affectées.

Pour ce faire, procédez comme suit :

1.  Configurez un nouveau site UDDI services v 3.0 sur un ordinateur déjà chargé avec Windows Server 2008 R2. (Remarque : dans une installation distribuée, un site UDDI v 3.0 peut être constitué de plusieurs ordinateurs Windows Server 2008 R2.)
2.  Utilisez l’outil de migration de données UDDI pour migrer les données de l’ancienne base de données des services UDDI vers la nouvelle base de données.
3.  Sauvegardez l’ancienne base de données des services UDDI pour garantir la restauration.
4.  Désinstallez les anciens logiciels des services UDDI, puis mettez-les à niveau vers Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Site Web des services Microsoft UDDI](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Spécifications UDDI](http://uddi.xml.org/specification)
-   [Téléchargement des services UDDI v 3.0 pour Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



