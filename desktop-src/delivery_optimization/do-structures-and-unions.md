---
title: Structures et unions d’optimisation de la remise
description: Les interfaces d’optimisation de la distribution utilisent les structures suivantes.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 035b465d61cfcee78a20fda0d275e1eece1a78c5
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520479"
---
# <a name="delivery-optimization-structures-and-unions"></a>Structures et unions d’optimisation de la remise

Les [interfaces](do-interfaces.md) d’optimisation de la distribution utilisent les structures suivantes.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | La structure **BG_FILE_PROGRESS** fournit des informations de progression relatives aux fichiers, telles que le nombre d’octets transférés. |
| [**BG_FILE_RANGE**](bg-file-range.md) | La structure **BG_FILE_RANGE** identifie une plage d’octets à télécharger à partir d’un fichier. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | La structure **BG_JOB_PROGRESS** fournit des informations de progression relatives aux tâches, telles que le nombre d’octets et de fichiers transférés. Pour les travaux de chargement, la progression s’applique au fichier de téléchargement, pas au fichier de réponse.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | La structure **BG_JOB_TIMES** fournit des horodatages liés aux travaux. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | L' **BITS_FILE_PROPERTY_VALUE** Union fournit la valeur de la propriété du fichier d’optimisation de la remise en fonction d’une valeur de l’énumération [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) . |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | L' **BITS_JOB_PROPERTY_VALUE** Union fournit la valeur de la propriété du travail d’optimisation de la remise en fonction de la valeur de l’énumération [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) . |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Utilisé par **IDOManager :: EnumDownloads** pour filtrer l’énumération downloads par la valeur de la propriété spécifique. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifie une seule plage d’octets à télécharger à partir d’un fichier. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifie un tableau de plages d’octets à télécharger à partir d’un fichier. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Permet d’obtenir l’état d’un téléchargement spécifique. |
| [**DOSwarmStats**](doswarmstats.md) | Contient des champs pour les statistiques de téléchargement et de téléchargement d’un fichier. |