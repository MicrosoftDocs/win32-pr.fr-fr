---
description: Décrit les points d’analyse.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Points d'analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867481"
---
# <a name="reparse-points"></a>Points d'analyse

Un fichier ou un répertoire peut contenir un *point d’analyse*, qui est une collection de données définies par l’utilisateur. Le format de ces données est compris par l’application qui stocke les données, et un filtre de système de fichiers que vous installez pour interpréter les données et traiter le fichier. Lorsqu’une application définit un point d’analyse, elle stocke ces données, ainsi qu’une *balise d’analyse*, qui identifie de façon unique les données qu’elle stocke. Lorsque le système de fichiers ouvre un fichier avec un point d’analyse, il tente de trouver le filtre de système de fichiers associé au format de données identifié par la balise d’analyse. Si un filtre de système de fichiers est trouvé, le filtre traite le fichier comme indiqué par les données d’analyse. Si un filtre de système de fichiers est introuvable, l’opération d’ouverture de fichier échoue.

Par exemple, les points d’analyse sont utilisés pour implémenter des liens de système de fichiers NTFS et le serveur de stockage étendu Microsoft (RSS). RSS utilise un ensemble de règles définies par l’administrateur pour déplacer des fichiers rarement utilisés vers un stockage à long terme, tel qu’une bande ou un support optique. Il utilise des points d’analyse pour stocker des informations sur le fichier dans le système de fichiers. Ces informations sont stockées dans un fichier stub qui contient un point d’analyse dont les données pointent vers l’appareil sur lequel le fichier réel se trouve maintenant. Le filtre de système de fichiers peut utiliser ces informations pour récupérer le fichier.

Les points d’analyse sont également utilisés pour implémenter des dossiers montés. Pour plus d’informations, consultez [déterminer si un répertoire est un dossier monté](determining-whether-a-directory-is-a-volume-mount-point.md).

Les restrictions suivantes s’appliquent aux points d’analyse :

-   Les points d’analyse peuvent être établis pour un répertoire, mais le répertoire doit être vide. Dans le cas contraire, le système de fichiers NTFS ne parvient pas à établir le point d’analyse. En outre, vous ne pouvez pas créer de répertoires ou de fichiers dans un répertoire qui contient un point d’analyse.
-   Les points d’analyse et les attributs étendus s’excluent mutuellement. Le système de fichiers NTFS ne peut pas créer un point d’analyse lorsque le fichier contient des attributs étendus, et il ne peut pas créer d’attributs étendus sur un fichier qui contient un point d’analyse.
-   Les données du point d’analyse, y compris la balise et le **GUID** facultatif, ne peuvent pas dépasser 16 kilo-octets. La définition d’un point d’analyse échoue si la quantité de données à placer dans le point d’analyse dépasse cette limite.
-   Il existe une limite de 63 points d’analyse sur un chemin d’accès donné.

    **Windows Server 2003 et Windows XP :** Il existe une limite de 31 points d’analyse sur un chemin d’accès donné.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Étiquettes de point d’analyse](reparse-point-tags.md)<br/>                                 | Chaque point d’analyse a une balise d’identificateur, ce qui vous permet de distinguer efficacement les différents types de points d’analyse, sans avoir à examiner les données définies par l’utilisateur dans le point d’analyse.<br/> |
| [Opérations de point d’analyse](reparse-point-operations.md)<br/>                     | Décrit les opérations de point d’analyse que vous pouvez effectuer à l’aide de [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).<br/>                                                                                       |
| [Points d’analyse et opérations sur les fichiers](reparse-points-and-file-operations.md)<br/> | Décrit comment les points d’analyse activent le comportement du système de fichiers qui fait partie du comportement de la plupart des développeurs Windows.<br/>                                                                                     |



 

 

