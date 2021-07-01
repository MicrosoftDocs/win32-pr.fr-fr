---
title: API de mastérisation d’image
description: API de mastérisation d’image
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119675"
---
# <a name="image-mastering-api"></a>API de mastérisation d’image

## <a name="purpose"></a>Objectif

L’API de mastérisation des images Microsoft Windows permet aux applications de préparer et de graver des images sur des supports de stockage sur CD, DVD et disques Blu-Ray. D’autres supports de type disque qui définissent les images de la même manière peuvent également utiliser cette API.

## <a name="developer-audience"></a>Développeurs concernés

IMAPi est conçu pour les développeurs C/C++ et Visual Basic, ainsi que pour ceux qui écrivent des scripts à l’aide de VBScript.

Il est recommandé d’avoir connaissance des technologies de CD, DVD et Blu-Ray et des systèmes de fichiers. Les développeurs peuvent bénéficier d’une bonne connaissance de la dernière révision de la commande multimédia (MMC) sur [ftp://ftp.T10.org/T10/drafts/MMC6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Conditions d’exécution

IMAPi 2,0 est pris en charge en mode natif à partir de Windows Vista et de Windows Server 2008. L’activation de la fonctionnalité IMAPi 2,0 pour Windows XP et Windows Server 2003 requiert l’installation du package de mise à jour [KB932716](https://support.microsoft.com/kb/932716) . Si ce package n’est pas installé, Windows XP prend en charge [imapi 1,0](imapiv1.md)en mode natif.

> [!Note]  
> Le Pack de fonctionnalités Windows pour le stockage est accessible au public par le biais du [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05). Vous trouverez des informations supplémentaires sur les modifications spécifiques de l’API dans la section [Nouveautés](what-s-new.md) .

 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                             | Description                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Nouveautés](what-s-new.md)<br/>           | Informations détaillant chaque version importante de l’API de mastérisation d’image.<br/> |
| [À propos d’IMAPi](about-imapi.md)<br/>         | Informations générales sur l’API de mastérisation d’image.<br/>                         |
| [Utilisation d’IMAPi](using-imapi.md)<br/>         | Rubriques relatives aux tâches qui montrent comment utiliser l’API de mastérisation d’image.<br/>   |
| [Référence IMAPi](imapi-reference.md)<br/> | Description détaillée des interfaces IMAPi et d’autres éléments de programmation.<br/>  |



 

## <a name="additional-resources"></a>Ressources supplémentaires

Vous trouverez des informations supplémentaires sur IMAPi et d’autres sujets connexes aux emplacements suivants :



| Rubrique                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blog Microsoft Optical Storage](/archive/blogs/opticalstorage/)                | Met en évidence les rubriques qui se concentrent sur l’implémentation de l’API de mastérisation d’image dans les scénarios de développement réel.                                                                                                                                                                                                                                                 |
| [Forum de discussion sur les plateformes optiques](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Discutez des problèmes de CDROM.SYS, IMAPIv2 et de système de fichiers en direct. Ce forum se concentre sur les rubriques au niveau du système et est destiné aux développeurs d’applications plutôt qu’à utilisateurs.                                                                                                                                                                                                 |
| [Comité technique de T10](https://www.t10.org/)                       | Un Comité technique du Comité InterNational des normes des technologies de l’information (INCITS, prononcé « Insights »). L’INCITS est homologué par et fonctionne selon les règles approuvées par le American National Standards Institute (ANSI). Ces règles sont conçues pour garantir que les normes volontaires sont développées par le consensus des groupes de l’industrie. |
| [Association de technologie de stockage optique (OSTA)](http://www.osta.org/) | Travaille à la mise en forme du futur du secteur grâce à des réunions régulières d’applications de stockage optique commercial (COSA), de compatibilité DVD, de marketing, MPV (MusicPhotoVideo), de comités UDF et d’un nouveau Comité Blue laser ad hoc. Les sociétés intéressées du monde entier sont invitées à rejoindre l’organisation et à participer à ses comités et à ses programmes.               |



 

 

