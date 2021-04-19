---
description: L’objectif de la reconnaissance du système de fichiers est de permettre au système d’exploitation Windows d’avoir une option supplémentaire pour un système de fichiers valide mais non reconnu, autre que &\# 0034 ; RAW&\# 0034 ;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Reconnaissance du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 457d4146588ba2db2b75d06c7afac10ecb18e87c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518400"
---
# <a name="file-system-recognition"></a>Reconnaissance du système de fichiers

L’objectif de la reconnaissance du système de fichiers est de permettre au système d’exploitation Windows d’avoir une option supplémentaire pour un système de fichiers valide mais non reconnu autre que « RAW ». Pour ce faire, à partir de Windows 7 et de Windows Server 2008 R2, le système définit un type de structure de données fixe qui peut être écrit sur le support sur lequel une technologie activée qui modifie le format du système de fichiers est active. Cette structure de données, si elle est présente sur le secteur du disque logique zéro, est alors reconnue par le système d’exploitation et informe l’utilisateur que le support contient un système de fichiers valide mais non reconnu et qu’il n’est pas un volume brut si les pilotes du système de fichiers ne sont pas installés.

## <a name="file-system-recognition-features-and-use"></a>Fonctionnalités et utilisation de la reconnaissance du système de fichiers

Plusieurs technologies de stockage récentes ont modifié le format du système de fichiers sur disque, de sorte que les supports sur lesquels ces technologies sont activées ne peuvent pas être reconnaissables aux versions antérieures de Windows, car les pilotes de système de fichiers ne sont pas existants lors de la publication d’une version antérieure particulière de Windows. Le comportement par défaut précédent dans ce scénario était le suivant. Lorsque le support de stockage n’est pas un système de fichiers connu, il est identifié comme étant brut, puis propagé vers le shell Windows, où la lecture automatique invite avec l’interface utilisateur de format. La reconnaissance du système de fichiers peut résoudre ce problème si les auteurs du nouveau système de fichiers écrivent correctement la [**structure de données**](file-system-recognition-structure.md) appropriée sur le disque.

La reconnaissance du système de fichiers utilise les fonctionnalités et couches suivantes dans le système d’exploitation pour atteindre ses objectifs :

-   Support de stockage, où une structure de données fixe réside sous la forme d’une séquence d’octets organisée en interne dans une structure prédéfinie appelée structure de données de [**structure de reconnaissance du système de fichiers \_ \_ \_**](file-system-recognition-structure.md) . Il incombe au développeur de système de fichiers de créer cette structure sur disque correctement.
-   La reconnaissance du système de fichiers au niveau de l’application, obtenue via l’utilisation du code de contrôle d’e/s du périphérique de [**reconnaissance du système de \_ fichiers de requête \_ \_ \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) . Pour obtenir un exemple d’utilisation de ce code de contrôle, consultez [obtention d’informations sur la reconnaissance du système de fichiers](obtaining-file-system-recognition-information.md).
-   Code de validation de la somme de contrôle, stocké dans la structure de données de la [**structure de reconnaissance du système de fichiers \_ \_ \_**](file-system-recognition-structure.md) . Pour obtenir un exemple illustrant la façon de calculer cette somme de contrôle, consultez [calcul de la somme de contrôle de la reconnaissance du système de fichiers](computing-a-file-system-recognition-checksum.md).
-   L’interface utilisateur du shell Windows utilise les fonctionnalités précédemment listées pour fournir une lecture automatique plus flexible et robuste et une prise en charge associée pour les systèmes de fichiers non reconnus, mais elle ne peut fonctionner que si la structure de données de la structure de reconnaissance du système de fichiers existe dans le secteur du disque logique zéro. [**\_ \_ \_**](file-system-recognition-structure.md) Les développeurs qui implémentent de nouveaux systèmes de fichiers doivent utiliser ce système pour s’assurer que leur système de fichiers n’est pas considéré par erreur comme étant de type « RAW ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Calcul d’une somme de contrôle de reconnaissance du système de fichiers](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Obtention d’informations sur la reconnaissance du système de fichiers](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Obtention d’informations sur le volume](obtaining-volume-information.md)
</dt> </dl>

 

 
