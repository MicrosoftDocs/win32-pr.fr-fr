---
title: Windows Programme d’installation pour les développeurs de jeux
description: cet article donne une vue d’ensemble des Windows Installer, spécifiquement destinés aux développeurs de jeux. pour obtenir une documentation détaillée sur les fonctionnalités et les api mentionnées dans cet article, consultez le kit de développement logiciel (SDK) Windows platform.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc587725ce2a2a675c9db835fabb503bc44ffa62c07ee1ce80578aef9432cf9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290389"
---
# <a name="windows-installer-for-game-developers"></a>Windows Programme d’installation pour les développeurs de jeux

montre comment les Windows Installer peuvent être utilisés pour installer des jeux sur les ordinateurs des utilisateurs finaux. Windows Le programme d’installation offre une prise en charge complète d’une interface utilisateur personnalisée, ainsi que des correctifs.

Microsoft Windows Installer est l’API par défaut pour l’installation de logiciels sur des ordinateurs basés sur Windows. bien que la plupart des fonctionnalités de Windows Installer soient conçues pour prendre en charge le déploiement d’applications métier dans un environnement d’entreprise, Windows Installer est également entièrement adapté à l’installation de jeux sur les ordinateurs des utilisateurs finaux. les principaux avantages de l’utilisation de Windows Installer pour l’installation de jeux sont les suivants :

-   Désinstallation fiable
-   Possibilité d’installer du contenu à la demande
-   Prise en charge d’une interface utilisateur entièrement personnalisée
-   Mise à jour corrective efficace

cet article donne une vue d’ensemble des Windows Installer, spécifiquement destinés aux développeurs de jeux. pour obtenir une documentation détaillée sur les fonctionnalités et les api mentionnées dans cet article, consultez le kit de développement logiciel (SDK) Windows platform.

-   [Vue d'ensemble](#overview)
-   [Concepts clés Windows Installer](#key-windows-installer-concepts)
    -   [Composants](#components)
    -   [Caractéristiques](#features)
-   [États d’installation](#install-states)
-   [Installer à la demande](#install-on-demand)
-   [Interface utilisateur personnalisée](#custom-user-interface)
-   [Application de correctifs](#patching)
-   [Autres ressources](#other-resources)

## <a name="overview"></a>Vue d’ensemble

toutes les configurations basées sur Windows Installer utilisent un fichier de base de données d’installation appelé fichier MSI pour décrire le mode d’installation de l’application. Le fichier MSI contient des informations sur les fichiers, les clés de Registre, les raccourcis de bureau, les associations de fichiers et autres éléments d’application à installer. Les fichiers réels à installer peuvent être compressés dans le fichier MSI lui-même, regroupés et compressés dans des « fichiers CAB » distincts, ou stockés ailleurs sur le support d’installation en tant que fichiers non compressés individuels. Le fichier MSI peut également faire référence à des actions personnalisées implémentées de manière externe, afin d’autoriser les actions pour lesquelles le fichier MSI n’est pas autorisé en mode natif.

Un fichier MSI peut éventuellement contenir une interface utilisateur pour guider l’utilisateur tout au long du processus d’installation. Cette interface utilisateur convient à la plupart des applications. toutefois, il a l’apparence d’une application Windows normale, et de nombreux développeurs préfèrent que leur application d’installation maintienne l’apparence du jeu lui-même, afin de fournir une expérience utilisateur final plus cohérente. pour prendre en charge ce scénario d’interface utilisateur entièrement personnalisé, une application de configuration peut désactiver l’interface utilisateur intégrée de Windows Installer et gérer l’intégralité de l’interface utilisateur elle-même. l’API Windows Installer expose un mécanisme de rappel pour permettre à une interface utilisateur de configuration personnalisée d’être informé de la progression de l’installation, ainsi que des événements importants tels que les demandes de modification de disque.

Windows Le programme d’installation n’est pas une solution de bout en bout pour la création de configurations. Il s’agit uniquement d’une API qui peut être utilisée par un programme d’installation pour effectuer l’installation réelle de fichiers, de clés de Registre, de raccourcis de bureau et d’autres éléments de l’application. les versions récentes de tous les principaux outils d’installation commerciaux (par exemple, InstallShield, WISE et Microsoft Visual Studio) prennent en charge Windows Installer. ces outils fournissent des interfaces utilisateur pratiques pour créer la configuration d’un jeu, mais ils s’appuient sur l’API Windows Installer pour effectuer une grande partie de l’installation. Ces outils peuvent également être utilisés uniquement pour créer une base de données MSI contenant le package d’installation, qui peut ensuite être installé à partir d’une interface utilisateur d’installation personnalisée. en guise d’alternative aux outils tiers, l’API Windows Installer fournit toutes les fonctions nécessaires à la création et à la manipulation d’une base de données msi par programme, et le kit de développement logiciel (SDK) de la plateforme Windows inclut un outil d’édition de base de données msi nu appelé Orca.

## <a name="key-windows-installer-concepts"></a>Concepts clés Windows Installer

voici les composants et fonctionnalités de Windows Installer.

### <a name="components"></a>Composants

Une application est constituée d’un ou de plusieurs composants, identifiés par un ID de composant GUID. Un composant est une unité atomique ; Il est entièrement installé ou n’est pas installé du tout. Un composant peut se composer d’un seul fichier, de plusieurs fichiers, de clés de Registre, de raccourcis de bureau ou d’une combinaison de ces éléments. Les ressources (fichiers, etc.) dans un composant doivent être uniques à ce composant. deux composants ne peuvent pas contenir la même ressource. Un composant n’est jamais installé explicitement ; Il n’est installé que dans le cadre d’une fonctionnalité (voir ci-dessous).

### <a name="features"></a>Fonctionnalités

Une fonctionnalité est un groupe de composants, identifié par un ID de fonctionnalité GUID. Contrairement aux composants, plusieurs fonctionnalités peuvent contenir le même composant. Un composant partagé entre plusieurs fonctionnalités sera installé si l’une de ces fonctionnalités est installée, et supprimée uniquement lorsque toutes les fonctionnalités qui font référence au composant ont été désinstallées. L’installation d’une fonctionnalité peut être effectuée automatiquement dans le cadre de l’installation d’un produit, ou elle peut être effectuée manuellement à l’aide de l’API [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) .

bien que peu de jeux aient plusieurs « fonctionnalités » qui peuvent être installées indépendamment, le concept Windows Installer d’une fonctionnalité est toujours utile. comme une fonctionnalité de Windows Installer n’est rien de plus qu’une collection de composants pouvant être installés ensemble, les jeux peuvent utiliser des fonctionnalités pour regrouper tout le contenu nécessaire pour une étape particulière du jeu. Par exemple, un jeu orienté niveau peut définir une fonctionnalité par niveau, comprenant tout le contenu requis pour ce niveau. Cela permettrait au jeu d’installer le contenu un niveau à la fois à partir du jeu lui-même, au lieu d’installer tout le contenu pour tous les niveaux lors de l’installation initiale.

## <a name="install-states"></a>États d’installation

Chaque composant ou fonctionnalité est associé à un état d’installation qui détermine si le composant ou la fonctionnalité est disponible et, le cas échéant, où sont installés les fichiers du composant ou de la fonctionnalité. Les États d’installation possibles pour une fonctionnalité sont les suivants :

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Manqu
</dt> <dd>

La fonctionnalité n’est pas installée et est donc inaccessible.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Localisé
</dt> <dd>

La fonctionnalité est disponible et est installée pour être exécutée à partir du disque dur local.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Code
</dt> <dd>

La fonctionnalité est disponible et est installée pour être exécutée à partir du support source d’origine (généralement un CD ou un DVD).

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Publiés
</dt> <dd>

La fonctionnalité n’est pas installée, mais peut être installée à la demande à l’aide de l’API [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) . Lorsque la fonctionnalité est effectivement installée, elle peut être installée à l’état local ou source.

</dd> </dl>

Un composant peut avoir l’un des États ci-dessus, à l’exception de « publié ». Si un composant fait partie d’une fonctionnalité publiée, le composant s’affiche comme « absent » jusqu’à ce que la fonctionnalité soit installée.

## <a name="install-on-demand"></a>Installer à la demande

Windows Le programme d’installation permet à une application de marquer les fonctionnalités comme publiées, ce qui signifie que la fonctionnalité n’est pas encore installée, mais qu’elle est disponible pour installation au moment de l’exécution, si nécessaire. L’installation des fonctionnalités au moment de l’exécution est appelée « installation à la demande ». Les jeux peuvent utiliser l’installation à la demande pour réduire considérablement le temps nécessaire à la configuration initiale du jeu en différant l’installation du contenu du jeu jusqu’à ce qu’il soit nécessaire au moment de l’exécution. Le délai nécessaire pour installer le contenu au moment de l’exécution peut souvent être partiellement ou complètement masqué en procédant à une installation à la demande dans un thread d’arrière-plan, tandis que l’utilisateur est occupé par le jeu.

## <a name="custom-user-interface"></a>Interface utilisateur personnalisée

bien que Windows Installer fournit une interface utilisateur par défaut qui guide l’utilisateur tout au long de l’installation de l’application, cette interface ressemble à celle d’une application de Windows standard. De nombreux développeurs de jeux préfèrent que leur interface utilisateur d’installation ait le même aspect que le jeu lui-même, afin de fournir à l’utilisateur un goût de la ambiance du jeu. pour prendre cela en charge, Windows Installer permet à l’interface utilisateur intégrée d’être complètement désactivée, ce qui permet au développeur de fournir une interface utilisateur entièrement personnalisée.

le programme d’installation personnalisée désactive d’abord l’interface utilisateur intégrée de Windows Installer à l’aide de l’API [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) pour définir le niveau de l’interface utilisateur sur INSTALLUILEVEL \_ NONE. Il appelle ensuite l’API [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) pour spécifier une fonction de rappel qui sera appelée au cours du processus d’installation pour notifier le programme d’installation des événements clés au cours de l’installation.

Le processus d’installation réel est ensuite démarré en appelant l’API [**MsiInstallProduct**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) . Cette API accepte une chaîne de paramètres qui permet à l’appelant de spécifier des valeurs pour les propriétés nommées. Ces propriétés peuvent être utilisées dans la base de données d’installation elle-même pour personnaliser la façon dont l’application doit être installée. Ces propriétés peuvent être utilisées pour spécifier les éléments suivants :

-   Répertoire dans lequel l’application doit être installée
-   Quelles fonctionnalités doivent être installées localement et qui doivent être installées pour être exécutées à partir du CD/DVD (par exemple, pour activer le choix entre une installation minimale et une installation complète)
-   Si l’application doit être installée pour tous les utilisateurs de l’ordinateur ou uniquement pour l’utilisateur actuel

Au cours de l’installation, le programme d’installation utilise les messages de notification envoyés à sa fonction de rappel pour déterminer quand mettre à jour son interface utilisateur de l’indicateur de progression, quand il doit inviter l’utilisateur à insérer le CD suivant, ou quand notifier l’utilisateur d’une erreur dans le processus d’installation.

## <a name="patching"></a>Application de correctifs

Windows Le programme d’installation permet d’appliquer des correctifs aux applications installées en appliquant un fichier correctif. Un fichier correctif contient les nouveaux fichiers à ajouter par le correctif, les fichiers modifiés par le correctif et une liste des modifications à apporter à la base de données d’installation. Pour économiser de l’espace, au lieu de stocker le contenu complet d’un fichier modifié par le correctif, le fichier correctif contient en fait uniquement les différences entre la version d’origine du fichier et la nouvelle version du fichier.

Pour créer un correctif, vous avez besoin de l’image d’installation de chacune des versions de l’application à partir desquelles vous souhaitez mettre à niveau le correctif, ainsi que de l’image d’installation de la nouvelle version mise à niveau de l’application. Une image de configuration se compose de la base de données MSI et de tous les fichiers de données réels pour l’application. La meilleure façon de créer une image d’installation pour une nouvelle version de l’application consiste à copier l’image d’installation à partir de la version précédente de l’application, puis à apporter toutes les modifications nécessaires pour mettre à jour cette copie vers la version corrigée.

Une fois que vous disposez de toutes les images d’installation nécessaires, vous pouvez créer les correctifs à l’aide de Msimsp.exe, qui est un outil de création de correctifs disponible dans le cadre du kit de développement logiciel (SDK) de la plateforme. L’outil vous demandera les emplacements de chacune des images d’installation, puis déterminera comment représenter efficacement les différences entre les versions successives. La sortie de l’outil est le dernier fichier correctif (identifié par le MSP de l’extension). Pour installer le correctif par programme, appelez l’API [**MsiApplyPatch**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) . L’utilisateur peut également installer le correctif manuellement en double-cliquant sur le fichier MSP dans l’Explorateur.

## <a name="other-resources"></a>Autres ressources

-   pour plus d’informations sur l’API Windows Installer, consultez [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Pour plus d’informations sur les meilleures pratiques pour l’installation de jeux, consultez [installation et maintenance des jeux](/windows/desktop/DxTechArts/installation-and-maintenance-of-games).

 

 