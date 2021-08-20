---
description: Les applications qui reposent sur des ressources réseau pour l’installation à la demande sont susceptibles d’échouer dans la source si l’emplacement source doit changer pour une raison quelconque ou être endommagé.
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: Résilience source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af1f3015296f4667f149a030cf06ea222ffa35c810f63440cfb0c20bde2e992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990024"
---
# <a name="source-resiliency"></a>Résilience source

Les applications qui reposent sur des ressources réseau pour [l’installation à la demande](installation-on-demand.md) sont susceptibles d’échouer dans la source si l’emplacement source doit changer pour une raison quelconque ou être endommagé. le Windows Installer fournit la résilience source pour les fonctionnalités installées à la demande à l’aide d’une liste source. La liste source contient les emplacements recherchés par le programme d’installation des packages d’installation. Les entrées de cette liste peuvent être des emplacements réseau, des URL (Uniform Resource Locators) ou des disques compacts. Si l’une de ces sources échoue, le programme d’installation peut essayer rapidement et en toute transparence la suivante.

Le développeur d’applications n’a pas besoin d’intégrer des informations spéciales dans le package d’installation pour garantir la résilience source. Une fois l’application installée, le programme d’installation a le comportement de l’ajout de la dernière source correctement utilisée en tant qu’entrée dans la liste source. Par défaut, cette source est l’emplacement à partir duquel le package d’installation est installé initialement, et est identique à la propriété [**SourceDir**](sourcedir.md) .

Un administrateur système peut modifier la liste source en appliquant une [transformation](merges-and-transforms.md) ou en modifiant la propriété [**SourceList**](sourcelist.md) à partir de la ligne de commande ou de la [table de propriétés](property-table.md).

Le programme d’installation commence à rechercher une source en vérifiant l’emplacement source utilisé le plus récemment dans la liste source. En cas d’échec de cette recherche, le programme d’installation recherche dans la liste des sources réseau, les sources de média et enfin les sources d’URL. Les administrateurs système peuvent modifier cet ordre de recherche à l’aide de la stratégie système [SearchOrder](searchorder.md) . Si ces recherches échouent, le programme d’installation peut présenter une [boîte de dialogue de navigation](browse-dialog.md) qui permet à l’utilisateur de rechercher la source manuellement. La boîte de dialogue Parcourir ne peut pas être affichée si le niveau de l’interface utilisateur est défini sur aucun. Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

En règle générale, le programme d’installation ne doit afficher une boîte de dialogue de navigation que si l’utilisateur actuel est un administrateur ou si l’installation ne requiert pas de privilèges élevés. Un administrateur peut contrôler l’affichage de la boîte de dialogue Parcourir pour les utilisateurs ayant les stratégies [DisableBrowse](disablebrowse.md) et [AllowLockDownBrowse](allowlockdownbrowse.md) . Un administrateur contrôle également si les utilisateurs peuvent installer des applications à partir de sources situées sur un support à l’aide des stratégies [DisableMedia](disablemedia.md) et [AllowLockDownMedia](allowlockdownmedia.md) . l’utilisation de ces stratégies dépend de la version de Windows Installer. Pour plus d’informations, consultez les rubriques suivantes :

-   [Stratégie de résilience source](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



