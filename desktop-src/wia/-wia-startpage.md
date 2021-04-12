---
description: L’acquisition d’images Windows (WIA) est la plateforme d’acquisition d’image continue de la famille de systèmes d’exploitation Windows à partir de Windows Millennium Edition (Windows Me) et Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Acquisition d’image Windows (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff1f3fb51a4c87d909637a90591336d9d2eb30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526421"
---
# <a name="windows-image-acquisition-wia"></a>Acquisition d’image Windows (WIA)

L’acquisition d’images Windows (WIA) est la plateforme d’acquisition d’image continue de la famille de systèmes d’exploitation Windows à partir de Windows Millennium Edition (Windows Me) et Windows XP.

-   [Introduction](#introduction)
-   [Avantages de l’acquisition d’images Windows 2,0](#benefits-of-windows-image-acquisition-20)
    -   [Pour les créateurs d’applications](#for-application-writers)
    -   [Pour les fabriques de périphériques](#for-device-manufactures)
    -   [Pour les utilisateurs du scanneur](#for-scanner-users)
-   [Développement de l’acquisition d’images Windows](#development-of-windows-image-acquisition)
-   [Vue d’ensemble de l’acquisition d’images Windows](#overview-of-windows-image-acquisition)
-   [Faits à propos de l’acquisition d’image Windows 2,0](#facts-about-windows-image-acquisition-20)
-   [Public destiné aux développeurs](#developer-audience)
-   [Spécifications d’exécution](#run-time-requirements)
-   [Rubriques WIA](#wia-topics)

## <a name="introduction"></a>Introduction

La plateforme WIA permet aux applications d’images/graphiques d’interagir avec le matériel de création d’images et normalise l’interaction entre les différentes applications et les différents scanneurs. Cela permet à ces différentes applications de communiquer avec ces différents scanneurs et d’interagir avec eux sans nécessiter que les rédacteurs d’applications et les fabricants de scanneurs personnalisent leurs applications ou pilotes pour chaque combinaison d’appareils d’application.

![graphique présentant l’architecture de base d’WIA comme couche bidirectionnelle entre les applications et les appareils d’imagerie. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Avantages de l’acquisition d’images Windows 2,0

WIA offre des avantages aux développeurs d’applications, aux fabricants de périphériques et aux utilisateurs de scanneurs qui doivent interagir avec le matériel de création d’images.

### <a name="for-application-writers"></a>Pour les créateurs d’applications

-   Windows exécute un processus de certification pour les pilotes WIA afin que les applications WIA soient compatibles au niveau de la base avec tous les scanneurs WIA.
-   Les pilotes WIA sont chargés dans le processus de service WIA, fournissant ainsi un environnement de pilote plus stable.
-   Les applications peuvent être lancées à partir du bouton analyse de l’analyseur via les événements Push pris en charge par le sous-système WIA.
-   Le WIA comprend un filtre de segmentation par défaut dont tous les pilotes peuvent tirer parti ; de cette façon, les applications n’ont pas besoin d’écrire du code pour l’analyse multirégion à des fins telles que la séparation d’un grand nombre de photos sur un scanneur à plat.

### <a name="for-device-manufactures"></a>Pour les fabriques de périphériques

-   Le processus de certification WIA du pilote permet aux développeurs de pilote d’établir que leur pilote est conforme à WIA.
-   Les pilotes WIA peuvent tirer parti d’un filtre de segmentation intégré, d’un filtre de traitement d’image et d’un gestionnaire d’erreurs, s’ils choisissent de le faire.
-   Les scanneurs WIA sont prêts à l’emploi sur Windows avec des applications d’analyse Windows telles que télécopie et numérisation Windows et Paint.
-   Les pilotes WIA offrent une meilleure intégration avec Windows, comme l’expérience complète de l’appareil.
-   La version Windows Vista comprend un pilote de classe WSD-WIA qui permet à tous les appareils conformes au protocole WS-Scan (Web Services for scanner) de fonctionner avec des applications WIA sans pilote ni logiciel supplémentaire.

### <a name="for-scanner-users"></a>Pour les utilisateurs du scanneur

-   Les scanneurs WIA peuvent être utilisés à partir d’applications Windows, telles que Windows Fax and Scan et Paint, sans nécessiter de logiciel supplémentaire.
-   Les applications et les scanneurs WIA peuvent également tirer parti des compléments WIA, tels que le filtre de segmentation, qui permet de traiter de nombreuses images sur le scanneur et de les analyser dans des fichiers individuels sans intervention de l’utilisateur.
-   Les appareils basés sur WIA offrent une intégration bien meilleure avec d’autres fonctionnalités de Windows, telles que la fonctionnalité Device stage pour Windows 7.
-   WIA offre une expérience d’analyse plus robuste, stable et fiable en isolant le pilote et l’application.

## <a name="development-of-windows-image-acquisition"></a>Développement de l’acquisition d’images Windows

L’architecture d’imagerie dans Windows 2000 et Windows 95 ou version ultérieure est constituée d’une abstraction matérielle de bas niveau, de l’architecture d’image continue (STI) et d’un ensemble d’API de haut niveau connu sous le nom de TWAIN. Dans Windows XP et Windows Me, WIA a été introduit. WIA est une architecture de création d’images qui s’appuie sur STI et ne nécessite pas TWAIN, bien que TWAIN soit toujours pris en charge avec WIA.

WIA 1,0 a été introduit dans Windows me et Windows XP et prend en charge les scanners, les appareils photo numériques et l’équipement vidéo numérique. WIA 2,0 a été publié avec Windows Vista. WIA 2,0 est ciblé vers les scanneurs, mais continue à offrir la prise en charge des applications et des appareils WIA 1,0 hérités via une couche de compatibilité WIA 1,0 à WIA 2,0 fournie par le service WIA. Toutefois, la prise en charge du contenu vidéo a été supprimée de WIA pour Windows Vista. Nous vous recommandons l’API des appareils mobiles Windows (WPD) pour les appareils photo numériques et l’équipement vidéo numérique à l’avenir. Les pilotes TWAIN WIA et 1,0 sont toujours pris en charge directement sur Windows Vista et Windows 7, ainsi que sur les pilotes de périphérique 2,0 WIA et les applications d’acquisition d’images natives.

## <a name="overview-of-windows-image-acquisition"></a>Vue d’ensemble de l’acquisition d’images Windows

WIA fournit une infrastructure qui permet à un appareil de présenter ses fonctionnalités uniques au système d’exploitation et permet aux applications d’images d’appeler ces fonctionnalités uniques.

La plateforme WIA comprend un protocole d’acquisition de données, un modèle de pilote de périphérique et une interface (DDI), une API et un service WIA dédié. La plateforme comprend également un ensemble de pilotes en mode noyau intégrés qui prennent en charge la communication avec les appareils d’images connectés localement via des interfaces USB, série/parallèle, SCSI et FireWire. Le sous-système WIA comprend également une couche de compatibilité transparente qui permet aux applications compatibles TWAIN d’utiliser les périphériques WIA-Driver.

Les appareils de création d’images connectés au réseau qui prennent en charge le protocole WSD (Web Services for Devices) peuvent également être utilisés à partir d’applications de création d’images compatibles WIA sur Windows Vista et Windows 7 prêts à l’emploi via un pilote de classe WSD-WIA fourni avec Windows Vista. Le pilote de classe convertit les appels WIA en appels WSD et vice versa, et fait en sorte que les applications WIA existantes fonctionnent avec des scanneurs WSD sans pilote supplémentaire.

Les pilotes WIA sont constitués d’un composant d’interface utilisateur et d’un composant de pilote de base, chargés dans deux espaces de processus différents : l’interface utilisateur dans l’espace de l’application et le noyau de pilote dans l’espace de service WIA. Le service s’exécute dans un contexte de système local sous Windows XP et s’exécute dans un contexte de service local à partir de Windows Server 2003 et Windows Vista pour renforcer la sécurité contre les bogues ou les pilotes malveillants.

![graphique illustrant l’architecture d’WIA et son mode de fonctionnement en tant que service.](images/wia-arch.png)

L’ensemble d’API WIA expose les applications d’acquisition d’images à la fonctionnalité matérielle d’acquisition d’images en fournissant la prise en charge des éléments suivants :

-   Énumération des appareils d’acquisition d’images disponibles.
-   Création de connexions à plusieurs appareils simultanément.
-   Interrogation des propriétés des appareils d’une manière standard et extensible.
-   Acquisition de données d’appareil à l’aide de mécanismes de transfert standard et hautes performances.
-   Gestion des propriétés d’image entre les transferts de données.
-   Notification de la gestion des événements d’État et d’analyse de l’appareil.

Windows a ajouté la prise en charge des scripts à WIA en publiant la bibliothèque Automation WIA dans 2002 qui a été incorporée dans Windows Vista en tant que couche d’automatisation WIA (Windows Image Acquisition) et qui continue à faire partie de Windows 7. La bibliothèque d’automatisation WIA offre des fonctionnalités d’acquisition d’images de bout en bout pour les environnements de développement d’applications compatibles Automation et des langages de programmation tels que Microsoft Visual Basic 6,0, Active Server pages (ASP), VBScript et C \# .

Pour Windows 7, les API WIA offrent une prise en charge supplémentaire pour compléter la prise en charge de l’analyse Push déjà existante.

-   Analyse initiée par l’appareil configuré automatiquement avec les paramètres d’analyse configurés au niveau du scanneur sur le panneau avant de l’appareil.
-   Sélection automatique de la source pour l’analyse initiée par l’appareil.

## <a name="facts-about-windows-image-acquisition-20"></a>Faits à propos de l’acquisition d’image Windows 2,0

-   Le mécanisme de transfert de données dans WIA 2,0 est basé sur le flux. L’abstraction de flux supprime la distinction entre les différents types de transfert et permet également l’échange de métadonnées mutuellement convenues entre l’appareil et l’application.
-   Le sous-système WIA 2,0 comprend également un module complémentaire de pilote de filtre pour le traitement d’images de base qui peut être éventuellement remplaçable par le pilote du scanneur, si le pilote choisit de fournir un filtre de traitement d’image personnalisé. Le filtre intégré permet de poster le traitement des images acquises via le scanneur. Le filtre de traitement d’image active également les préversions logicielles en direct lorsque des petits paramètres tels que la luminosité et le contraste sont ajustés.
-   Le filtre de segmentation est un autre composant WIA pratique qui peut être remplacé par un filtre plus personnalisé par le pilote du scanneur. Le filtre de segmentation peut être utilisé pour l’analyse de plusieurs régions. L’analyse multirégion, par exemple, permet à une application de détecter automatiquement les différentes régions d’analyse sans aucune intervention de l’utilisateur, comme l’identification d’une série de photos qui se trouvent au hasard sur le plateau du scanneur.
-   WIA 2,0 fournit un gestionnaire d’erreurs remplaçables/extensible pour gérer correctement et éventuellement récupérer à partir de, des erreurs de logiciel, de matériel et de configuration et des retards. Le gestionnaire d’erreurs est un autre composant WIA qui peut être remplacé par le pilote de scanneur avec une version plus personnalisée. Cette extension fournit des messages d’État et d’erreur pendant les acquisitions de données telles que « préchauffage de la lampe », « couverture ouverte », « bourrage papier », etc. Cette extension permet également une prise en charge plus propre des « opérations d’annulation ».

## <a name="developer-audience"></a>Public de développeurs

L’API WIA est conçue pour être utilisée par les programmeurs C/C++. Vous devez vous familiariser avec l’interface utilisateur graphique Windows et les interfaces COM (Component Object Model).

Pour les développeurs familiarisés avec Microsoft Visual Basic 6,0, Active Server pages (ASP) ou la création de scripts, WIA fournit une couche d’automatisation pour Windows XP Service Pack 1 (SP1) ou version ultérieure qui s’appuie sur et simplifie l’accès aux fondations fournies par C/C++. Pour plus d’informations sur la couche Automation, consultez couche d’automatisation de l' [acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> La couche Automation WIA remplace les scripts WIA (Windows Image Acquisition) 1,0.

 

## <a name="run-time-requirements"></a>Exigences d'exécution

Les applications qui utilisent l’API WIA requièrent Windows XP ou une version ultérieure.

## <a name="wia-topics"></a>Rubriques WIA

Les rubriques WIA sont organisées comme indiqué dans le tableau suivant.



|                                                                                                                              |                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [À propos de l’acquisition d’images Windows](-wia-about-windows-image-acquisition.md)                                                  | Informations générales sur WIA                                                                     |
| [Pilotes d’acquisition d’images Windows](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Développement de pilotes WIA                                                                            |
| [Couche d’automatisation d’acquisition d’images Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Couche Automation WIA                                                                              |
| [Didacticiel WIA](-wia-wia-tutorial.md)                                                                                        | Procédure pas à pas du code inclus dans le kit de développement logiciel (SDK) qui se concentre sur des tâches spécifiques |
| [Référence](-wia-reference.md)                                                                                              | Informations sur les interfaces, méthodes, objets et types de données WIA utilisés dans C/C++ et les scripts.      |



 

 

 
