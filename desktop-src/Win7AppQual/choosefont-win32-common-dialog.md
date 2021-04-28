---
description: ChooseFont () boîte de dialogue commune Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () boîte de dialogue commune Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088607"
---
# <a name="choosefont-win32-common-dialog"></a>ChooseFont () boîte de dialogue commune Win32

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -faible  
**Fréquence** -moyenne  




## <a name="description"></a>Description

Windows 7 comprend plusieurs mises à jour de la boîte de dialogue commune Win32 ChooseFont (). Elles se répartissent en deux catégories :

-   Actualisation visuelle de la boîte de dialogue
-   Prise en charge des nouvelles fonctionnalités afficher/masquer les polices

La **boîte de dialogue actualiser** met à jour le modèle standard pour que la boîte de dialogue soit plus en ligne avec d’autres dispositions de dialogue dans Windows. Il introduit le WYSIWYG dans les listes d’affichage des polices pour aider les utilisateurs à choisir des polices. Il comprend également un lien vers le CPL des polices pour fournir un accès facile aux utilisateurs souhaitant personnaliser leurs listes de polices.

**Afficher/masquer les polices** est une nouvelle fonctionnalité de la plateforme Windows 7, dans laquelle les polices non appropriées pour les paramètres de langue de l’utilisateur actuel (méthodes d’entrée) ne sont pas présentées par défaut dans les listes de sélection de polices. Les utilisateurs peuvent personnaliser les polices qu’ils souhaitent voir apparaître dans le CPL des polices ou désactiver cette fonctionnalité.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

**Actualisation visuelle de la boîte de dialogue**

Nous avons introduit deux nouveaux modèles dans Windows 7 (un pour les applications qui chargent la version 6 ou ultérieure de comctl32.dll et une autre pour les applications qui chargent des versions antérieures).

-   Pour des raisons de compatibilité des applications, ces nouveaux modèles sont chargés uniquement pour les applications qui ne raccordent pas la file d’attente de messages ChooseFont. Les applications qui raccordent la file d’attente de messages continuent de voir l’ancienne disposition de boîte de dialogue.
-   Les applications qui fournissent leurs propres modèles continuent à pouvoir les utiliser.

Les applications qui n’obtiennent pas les nouveaux modèles ne voient pas les modifications de disposition de la boîte de dialogue à partir de Vista. Ils doivent toutefois toujours obtenir la nouvelle version préliminaire de la police WYSIWYG.

**Afficher/masquer les polices**

Pour toutes les versions de ChooseFont, la boîte de dialogue utilisera les paramètres afficher/masquer la police de l’utilisateur actuel pour déterminer la liste de polices à afficher. Cela entraîne l’affichage de moins de listes de polices dans la plupart des instances.

## <a name="end-user-mitigation"></a>Atténuation des utilisateurs finaux

**Afficher/masquer les polices :** Pour désactiver le masquage de la police, les utilisateurs doivent accéder à la page Paramètres des polices dans le CPL des polices et désélectionner l’option

Case à cocher « Masquer les polices en fonction des paramètres de langue »

## <a name="developer-mitigation"></a>Atténuation des développeurs

-   **Actualisation visuelle :** Les développeurs d’applications qui fournissent leurs propres modèles peuvent souhaiter l’actualiser pour qu’ils soient conformes au nouveau modèle Windows 7 approprié. Les nouveaux modèles sont disponibles dans le fichier de modèle font. dlg.

    **Remarque :** Le nouveau modèle publié contient un contrôle SysLink supplémentaire qui fournit un raccourci permettant aux utilisateurs de lancer le CPL des polices pour afficher plus de polices. Le contrôle de lien requiert la version 6 de la bibliothèque de contrôles communs Windows (comctl32.dll). Les développeurs doivent fournir un manifeste ou une directive qui spécifie l’utilisation de la version 6 de la DLL si elle est disponible. Lorsqu’une application utilise une version antérieure de la bibliothèque de contrôles communs, utilisez le type de contrôle « PUSHBUTTON » à la place.

-   **Afficher/masquer les polices :** Les développeurs peuvent désactiver cette fonctionnalité en fournissant un indicateur supplémentaire (CF \_ INACTIVEFONTS) dans le membre Flags de la structure CHOOSEFONT. La définition de cet indicateur entraîne l’affichage de toutes les polices installées dans la liste police.
-   **Afficher/masquer les polices :** Les applications qui fournissent du contenu d’aide ChooseFont peuvent souhaiter ajouter du contenu pour expliquer pourquoi la liste de polices est réduite et diriger les utilisateurs vers le CPL des polices pour personnaliser leurs listes de polices.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

Les développeurs dont les applications raccordent la file d’attente de messages ChooseFont pour personnaliser la boîte de dialogue doivent vérifier que leurs applications conservent toutes les fonctionnalités existantes.

Les applications qui découpent fortement la liste de polices à l’aide d’indicateurs doivent s’assurer que la liste de polices présentée reste acceptable.

 

 



