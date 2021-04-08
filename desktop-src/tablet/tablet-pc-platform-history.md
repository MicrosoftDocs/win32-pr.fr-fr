---
description: Cette section décrit l’historique des versions de la technologie Tablet PC.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Historique de la plateforme Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f258876f79f8e701ed59242233dcccc292b15f52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035175"
---
# <a name="tablet-pc-platform-history"></a>Historique de la plateforme Tablet PC

Cette section décrit l’historique des versions de la technologie Tablet PC.

## <a name="platform-description"></a>Description de la plateforme

Les composants de la technologie Tablet PC vous permettent de développer des applications conçues pour le matériel Tablet PC.

Ces composants peuvent être utilisés pour créer des applications qui s’exécutent sur Windows XP Édition Tablet PC 2005, Windows Vista, Windows 7, Windows Server 2008 R2 et certains autres systèmes d’exploitation antérieurs.

Le Windows Presentation Foundation prend également en charge le développement d’applications Tablet PC.

## <a name="version-history"></a>Historique des versions

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Plateforme de tablette dans Windows 7 et Windows Server 2008 R2

Windows 7 introduit une prise en charge linguistique supplémentaire, le contrôle d’entrée mathématique et des dictionnaires personnalisés. Les fonctionnalités [tactiles Windows](../wintouch/windows-touch-portal.md) ont également été ajoutées aux systèmes d’exploitation Windows.

Windows Server 2008 R2 introduit la prise en charge de langues supplémentaires, de dictionnaires personnalisés et de la reconnaissance côté serveur.

Les fonctionnalités suivantes améliorent les fonctionnalités des tablettes et permettent aux développeurs de proposer de nouvelles applications qui prennent en charge des scénarios pratiques pour les utilisateurs finaux.

-   Le contrôle d’entrée mathématique permet d’entrer des formules mathématiques et des fonctions à partir de texte manuscrit dans Windows 7.
-   Dans le but d’améliorer la reconnaissance de texte, Windows 7 et Windows Server 2008 R2 prennent en charge les dictionnaires personnalisés afin que les administrateurs puissent directement activer la prise en charge des listes de mots.
-   Le tactile Windows prend en charge l’entrée de plusieurs sources tactiles à l’aide de nouveaux messages de fenêtre, en plus d’une API de reconnaissance de mouvement qui prend en charge le panoramique, le zoom et la rotation.
-   Windows Server 2008 R2 prend en charge la reconnaissance côté serveur des entrées de formulaire et prend également en charge les dictionnaires personnalisés pour la reconnaissance côté serveur. Grâce à l’ajout de ces fonctionnalités, les développeurs et les administrateurs peuvent créer et personnaliser des applications puissantes qui prennent en charge la reconnaissance de l’écriture manuscrite du côté serveur.

### <a name="tablet-platform-in-windows-vista"></a>Plateforme de tablette dans Windows Vista

Les fichiers binaires de la technologie Tablet PC ont été mis à jour dans Windows Vista. La technologie Tablet PC mise à jour comprend de nouvelles API d’analyse d’encre et une version COM des API d’entrée de stylet. Les applications écrites par rapport aux versions précédentes de la technologie Tablet PC s’exécutent sur Windows Vista sans modification.

Les composants de la technologie Tablet PC sont uniquement disponibles dans le cadre de la SDK Windows à partir de la sortie de Windows Vista. Pour plus d’informations, consultez [Nouveautés du développement Tablet PC](what-s-new-in-tablet-pc-development.md).

### <a name="version-17"></a>Version 1,7

Tablet PC Development Kit 1,7 étendu la fonctionnalité de développement au-delà de celle disponible dans la version 1,5, en ajoutant les API d’entrée de stylet et la prise en charge de l’encre sur le Web.

Dans le passé, la fonctionnalité de la version 1,5 était dans un fichier binaire séparé, mais dans le kit de développement Tablet PC 1,7, toutes les fonctionnalités étaient placées dans un seul fichier binaire.

### <a name="version-15"></a>Version 1.5

La version 1,5 du kit de développement est remplacée par la version 1,1. Elle fournissait des API du panneau de saisie Pen et l’objet diviseur.

> [!Note]  
> Si vous installez le kit de développement Tablet PC version 1,5, après l’installation, vous devez rétablir les références à l’assembly Microsoft Ink dans les applications écrites par rapport aux versions précédentes du kit de développement logiciel (SDK) Tablet PC avant de le compiler et de l’exécuter.

 

### <a name="version-11"></a>Version 1.1

La version 1,1 du kit de développement est remplacée par la version 1,0. La version 1,1 est composée uniquement de mises à jour de la documentation. les binaires de la plateforme n’ont pas été modifiés entre la version 1,1 du kit de développement et la version commercialisée de Windows XP Édition Tablet PC. Par conséquent, les applications développées avec le kit de développement de la version 1,1 n’ont pas besoin de redistribuer les composants pour utiliser les fonctionnalités de la plateforme lorsqu’elles sont installées sur les Tablet PC.

> [!Note]  
> Les applications distribuées aux systèmes d’exploitation non-Tablet PC peuvent utiliser un sous-ensemble de fonctionnalités de la plateforme Tablet PC. Ces applications doivent inclure le module de fusion redistribué fourni dans le kit de développement version 1,1 avec leur installation.

 

### <a name="version-10"></a>Version 1.0

La version 1,0 du kit de développement a été remplacée par la version 1,1.

 

 
