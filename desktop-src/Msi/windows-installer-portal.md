---
description: Moteur d’installation utilisé pour installer des applications ou des mises à jour ou des services exécutés sur Windows. Configure et répare les applications installées. Écrire des packages MSI personnalisés pour créer une installation exe ou une mise à jour ou une mise à niveau pour une application.
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: d818a3decc7cbede527929dc3756ba2edf193421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530586"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> Cette documentation est destinée aux développeurs de logiciels qui souhaitent utiliser Windows Installer pour créer des packages d’installation pour les applications. Si vous recherchez un package redistribuable pour Windows Installer 4,5 et versions antérieures, consultez [cet article](windows-installer-redistributables.md). Notez qu’il n’existe aucun redistribuable pour Windows Installer 5,0. Cette version est incluse avec le système d’exploitation dans les versions client et serveur de Windows 7, Windows Server 2008 R2 et versions ultérieures (y compris Windows 10).

Microsoft Windows Installer est un service d’installation et de configuration fourni avec Windows. Le service d’installation permet aux clients de fournir un meilleur déploiement d’entreprise et fournit un format standard pour la gestion des composants. Le programme d’installation active également la publication d’applications et de fonctionnalités selon le système d’exploitation. Pour plus d’informations, consultez [prise en charge des plateformes de la publication](platform-support-of-advertisement.md).

Cette documentation décrit Windows Installer 5,0 et versions antérieures. Toutes les fonctionnalités disponibles dans les versions ultérieures de Windows Installer ne sont pas disponibles dans les versions antérieures. Cette documentation ne décrit pas les versions antérieures à Windows Installer 2,0. Les packages d’installation et les correctifs créés pour Windows Installer 2,0 peuvent toujours être installés à l’aide de Windows Installer 3,0 et versions ultérieures.

Windows Installer 3,0 et versions ultérieures, peut installer plusieurs correctifs avec une seule transaction qui intègre la progression de l’installation, la restauration et les redémarrages. Le programme d’installation peut appliquer des correctifs dans un ordre spécifié, indépendamment de l’ordre dans lequel les correctifs sont fournis au système. L’application de correctifs à l’aide de Windows Installer 3,0 met à jour uniquement les fichiers affectés par le correctif et peut être beaucoup plus rapide que les versions antérieures du programme d’installation. Les correctifs installés avec Windows Installer 3,0 ou une version ultérieure peuvent être désinstallés dans n’importe quel ordre afin de conserver l’état du produit comme si le correctif n’avait jamais été installé. Les comptes avec des privilèges d’administrateur peuvent utiliser l’API de Windows Installer 3,0 et versions ultérieures pour interroger et inventorier des informations sur les produits, les fonctionnalités, les composants et les correctifs. Le programme d’installation peut être utilisé pour lire, modifier et remplacer des listes sources pour les sources de réseau, d’URL et de média. Les administrateurs peuvent énumérer les contextes d’utilisateur et d’installation et gérer les listes de sources à partir d’un processus externe.

Windows Installer 4,5 et versions ultérieures peuvent installer plusieurs packages d’installation à l’aide du [*traitement des transactions*](t-gly.md). Si tous les packages de la transaction ne peuvent pas être installés avec succès, ou si l’utilisateur annule l’installation, les Windows Installer peuvent restaurer les modifications et restaurer l’ordinateur à son état d’origine. Le programme d’installation s’assure que tous les packages appartenant à une transaction à plusieurs packages sont installés ou qu’aucun des packages n’est installé.

À partir de Windows Installer 5,0, un package peut être créé pour sécuriser les nouveaux comptes, les [services](../services/services.md)Windows, les fichiers, les dossiers et les clés de registre. Le package peut spécifier un descripteur de sécurité qui refuse des autorisations, spécifie l’héritage des autorisations d’une ressource parent ou spécifie les autorisations d’un nouveau compte. Pour plus d’informations, consultez [sécurisation des ressources](securing-resources-.md). Le service Windows Installer 5,0 peut énumérer tous les composants installés sur l’ordinateur et obtenir le chemin d’accès à la clé du composant. Pour plus d’informations, consultez [énumération de composants](enumerating-components-.md). À [l’aide](using-services-configuration.md)de la configuration des services, Windows Installer packages 5,0 peuvent personnaliser les services sur un ordinateur. Les développeurs du programme d’installation peuvent utiliser Windows Installer 5,0 et la création d’un [package unique](single-package-authoring.md) pour développer des packages d’installation uniques capables d’installer une application dans le [contexte d’installation](installation-context.md)par ordinateur ou par utilisateur.

## <a name="where-applicable"></a>Le cas échéant

Windows Installer permet d’installer et de configurer efficacement vos produits et applications s’exécutant sur Windows. Le programme d’installation fournit de nouvelles fonctionnalités permettant de publier des fonctionnalités sans les installer, d’installer des produits à la demande et d’ajouter des personnalisations utilisateur.

Windows Installer 5,0 s’exécutant sur Windows Server 2012 ou Windows 8 prend en charge l’installation d’applications approuvées sur Windows RT. Un package Windows Installer, un correctif ou une transformation qui n’a pas été signé par Microsoft ne peut pas être installé sur Windows RT. La propriété [**Résumé du modèle**](template-summary.md) indique la plateforme qui est compatible avec une base de données d’installation et, dans ce cas, doit inclure la valeur pour Windows RT.

Windows Installer est destiné au développement d’applications de style bureau.

## <a name="developer-audience"></a>Développeurs concernés

Cette documentation est destinée aux développeurs de logiciels qui souhaitent créer des applications qui utilisent Windows Installer. Il fournit des informations générales générales sur les packages d’installation et le service d’installation. Elle contient une description complète de l’interface de programmation d’applications et des éléments de la base de données du programme d’installation. Cette documentation contient également des informations supplémentaires pour les développeurs qui souhaitent utiliser un éditeur de table ou un outil de création de package pour effectuer ou gérer une installation.

## <a name="run-time-requirements"></a>Conditions d’exécution

Windows Installer 5,0 est inclus avec, Windows 7, Windows Server 2008 R2 et versions ultérieures. Il n’existe aucun redistribuable pour Windows Installer 5,0.

Les versions antérieures à Windows Installer 5,0 étaient fournies avec Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP et Windows 2000. [Windows Installer redistribuables](windows-installer-redistributables.md) sont disponibles pour Windows Installer 4,5 et certaines versions antérieures.

* Windows Installer 4,5 requiert Windows Server 2008, Windows Vista, Windows XP avec Service Pack 2 (SP2) et versions ultérieures, et Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures.

* Windows Installer 4,0 requiert Windows Vista ou Windows Server 2008. Il n’existe aucun redistribuable pour l’installation de Windows Installer 4,0 sur d’autres systèmes d’exploitation. Une version mise à jour de Windows Installer 4,0, qui n’ajoute pas de nouvelles fonctionnalités, est disponible dans Windows Vista avec Service Pack 1 (SP1) et Windows Server 2008.

* Windows Installer 3,1 requiert Windows Server 2003, Windows XP ou Windows 2000 avec Service Pack 3 (SP3).

* Windows Installer 3,0 requiert Windows Server 2003, Windows XP ou Windows 2000 avec SP3. Windows Installer 3,0 est inclus dans Windows XP avec Service Pack 2 (SP2). Il est disponible en tant que redistribuable pour Windows 2000 Server avec Service Pack 3 (SP3) et Windows 2000 Server avec Service Pack 4 (SP4), Windows XP RTM et Windows XP avec Service Pack 1 (SP1) et Windows Server 2003 RTM.

* Windows Installer 2,0 est contenu dans Windows Server 2003 et Windows XP.

* Windows Installer 2,0 est disponible en tant que package pour l’installation ou la mise à niveau vers Windows Installer 2,0 sur Windows 2000. Ce package ne doit pas être utilisé pour installer ou mettre à niveau Windows Installer 2,0 sur Windows Server 2003 et Windows XP.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Feuille de route](roadmap-to-windows-installer-documentation.md)<br/>                        | Guide de Windows Installer documentation.<br/>       |
| [Vue d’ensemble](about-windows-installer.md)<br/>                                          | Informations générales sur le programme d’installation.<br/>          |
| [Nouveautés de Windows Installer](what-s-new-in-windows-installer.md)<br/>           | Répertorie les ajouts et les modifications apportées à Windows Installer.<br/> |
| [Référence](installer-function-reference.md)<br/>                                    | Documentation des fonctions de Windows Installer.<br/>     |
| [Exemples de scripts Windows Installer](windows-installer-scripting-examples.md)<br/> | Windows Installer des exemples à l’aide d’un script.<br/>          |



 

 

 
