---
title: Structures et unions BITS
description: Les interfaces Service de transfert intelligent en arrière-plan (BITS) utilisent les structures suivantes.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 93763daa73bc96e12dd27b862d75fbb23869c20f
ms.sourcegitcommit: 31f494fef71b63ad411b86b22b4cc01af6e37c8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "104311662"
---
# <a name="bits-structures-and-unions"></a>Structures et unions BITS

Les [interfaces](bits-interfaces.md) service de transfert intelligent en arrière-plan (bits) utilisent les structures suivantes.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifie la cible (proxy ou serveur), le schéma d’authentification et les informations d’identification de l’utilisateur à utiliser pour les demandes d’authentification de l’utilisateur. La structure est transmise à la [méthode IBackgroundCopyJob2 :: SetCredentials](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials). |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifie les informations d’identification à utiliser pour le schéma d’authentification spécifié dans la [structure BG_AUTH_CREDENTIALS](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials). |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifie le nom d’utilisateur et le mot de passe à authentifier. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Fournit les noms locaux et distants du fichier à transférer. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Fournit des informations de progression relatives aux fichiers, telles que le nombre d’octets transférés. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifie une plage d’octets à télécharger à partir d’un fichier. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Fournit des informations relatives à la progression du travail, telles que le nombre d’octets et de fichiers transférés. Pour les travaux de chargement, la progression s’applique au fichier de téléchargement, pas au fichier de réponse. Pour afficher la progression du fichier de réponse, consultez la [structure BG_JOB_REPLY_PROGRESS](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Fournit des informations de progression relatives à la partie réponse d’une tâche de chargement-réponse. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Fournit des horodatages liés aux travaux. |
| [**BITS_FILE_PROPERTY_VALUE Union**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fournit la valeur de propriété d’un fichier BITS. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fournit la valeur de la propriété du travail BITS en fonction de la valeur de l' [énumération BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id). |
