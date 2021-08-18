---
title: Fonctions de mots clés dynamiques de pare-feu
description: Les mots clés dynamiques de pare-feu contiennent les fonctions suivantes.
keywords:
- Mots clés dynamiques de pare-feu, fonctions
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: 1aacc30ecac9cddca5f986878da1ff633660152144e8ca2fe1440fdecfd61e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015649"
---
# <a name="firewall-dynamic-keywords-functions"></a>Fonctions de mots clés dynamiques de pare-feu

Les mots clés dynamiques de pare-feu contiennent les fonctions suivantes.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Demande la remise des notifications concernant les modifications apportées à des objets d’adresse de mot clé dynamique ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) particuliers. |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Annule la remise des notifications concernant les modifications apportées à des objets d’adresse de mot clé dynamique ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) particuliers. |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Type de pointeur fonction du point d’entrée dans le service que vous appelez pour ajouter l’adresse de mot clé dynamique spécifiée. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Type de pointeur fonction du point d’entrée dans le service que vous appelez pour supprimer l’adresse de mot clé dynamique avec l’ID spécifié. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Type de pointeur fonction du point d’entrée dans le service que vous appelez pour énumérer les adresses de mots clés dynamiques spécifiques par ID. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Type de pointeur fonction du point d’entrée dans le service que vous appelez pour énumérer les adresses de mots clés dynamiques par type. Vous pouvez demander un sous-ensemble particulier d’objets en fonction des indicateurs d’énumération transmis. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Le type de pointeur de fonction du point d’entrée dans le service que vous appelez pour le mot de passe dynamique gratuit adresse des structs de données alloués par le service. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Type de pointeur fonction du point d’entrée dans le service que vous appelez pour mettre à jour l’adresse de mot clé dynamique avec l’ID d’entrée. |

## <a name="related-topics"></a>Rubriques connexes

* [Référence des mots clés dynamiques du pare-feu](firewall-dynamic-keywords-reference.md)
