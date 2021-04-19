---
description: 'Pour obtenir un handle vers un volume en vue d’une utilisation avec des opérations de journal des modifications du numéro de séquence de mise à jour (USN), appelez la fonction CreateFile avec le paramètre lpFileName défini sur une chaîne au format suivant : \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtention d’un handle de volume pour les opérations de journal des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529463"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a><span data-ttu-id="599cd-103">Obtention d’un handle de volume pour les opérations de journal des modifications</span><span class="sxs-lookup"><span data-stu-id="599cd-103">Obtaining a Volume Handle for Change Journal Operations</span></span>

<span data-ttu-id="599cd-104">Pour obtenir un handle vers un volume en vue d’une utilisation avec des opérations de journal des modifications du numéro de séquence de mise à jour (USN), appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec le paramètre *lpFileName* défini sur une chaîne au format suivant : \\ \\ . \\ *X*:</span><span class="sxs-lookup"><span data-stu-id="599cd-104">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*:</span></span>

<span data-ttu-id="599cd-105">Notez que *X* est la lettre qui identifie le lecteur sur lequel le volume NTFS s’affiche.</span><span class="sxs-lookup"><span data-stu-id="599cd-105">Note that *X* is the letter that identifies the drive on which the NTFS volume appears.</span></span>

<span data-ttu-id="599cd-106">Si le volume n’a pas de lettre de lecteur, utilisez la syntaxe décrite dans [attribution d’un nom à un volume](naming-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="599cd-106">If the volume does not have a drive letter, use the syntax described in [Naming a Volume](naming-a-volume.md).</span></span>

 

 



