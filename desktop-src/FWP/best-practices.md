---
title: Meilleures pratiques (plateforme de filtrage Windows)
description: La liste suivante contient les meilleures pratiques pour le développement d’applications à l’aide de l’API WFP (Windows Filtering Platform).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508249"
---
# <a name="best-practices-windows-filtering-platform"></a>Meilleures pratiques (plateforme de filtrage Windows)

La liste suivante contient les meilleures pratiques pour le développement d’applications à l’aide de l’API WFP (Windows Filtering Platform).

-   Utilisez des sessions dynamiques.

    De nombreuses applications ajoutent des objets de stratégie de filtrage au démarrage, puis suppriment ces objets à l’arrêt. En utilisant une session dynamique, vous garantissez que ces objets sont supprimés même si l’application se bloque. En outre, il est plus efficace de simplement fermer le handle de moteur à l’arrêt que d’effectuer des appels individuels pour supprimer chaque objet.

-   Gérez les délais d’attente des transactions de manière appropriée ou définissez la session **txnWaitTimeoutInMSec** sur Infinite afin d’éviter les délais d’attente.

    Même si vous n’utilisez pas de transactions explicites, la plupart des appels sont toujours exécutés dans le cadre d’une transaction implicite et peuvent donc avoir un délai d’attente.

-   Utilisez des transactions explicites pour combiner des opérations d’ajout ou de suppression liées dans une transaction unique.

    Cela est plus efficace et facilite le nettoyage des résultats partiels dans les chemins d’erreur.

-   Utilisez des chaînes compatibles avec MUI.

    Toutes les chaînes localisables sont stockées dans une structure de données commune : [**FWPM \_ Display \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Les chaînes de cette structure peuvent être des chaînes indirectes du type pris en charge par [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Avant qu’une structure **\_ \_ DATA0 d’affichage FWPM** ne soit retournée par l’une des fonctions, les chaînes indirectes sont résolues en la ressource de chaîne spécifiée à l’aide des paramètres régionaux de l’appelant.

-   Associez tous les objets à un fournisseur.

    Lorsque plusieurs fournisseurs sont installés sur le système, il est plus facile pour les outils de diagnostic de déterminer qui a ajouté quoi.

-   Ajoutez des filtres à votre propre sous-couche.

    Une fois qu’un filtre de fin dans une sous-couche est atteint, aucun autre filtre dans cette sous-couche n’est évalué. Ainsi, si vous ajoutez vos filtres à la même sous-couche qu’un autre fournisseur, vous risquez d’empêcher l’appel de ces filtres, ce qui aboutit à des résultats inattendus.

-   Utilisez la contrainte de mise en conformité de la couche application (ALE) plutôt que le filtrage orienté paquets.

    Le filtrage au niveau de la couche de paquets est lent.

-   Filtrez les erreurs ICMP et les événements RST avant qu’ils ne soient générés.

    Il est plus efficace de filtrer ces événements une fois qu’ils sont générés.

-   Effectuer l’inspection des paquets au niveau de la couche de données de flux/datagramme plutôt qu’au niveau de la couche de transport.

    Cela s’applique au développement de légendes. Pour plus d’informations, consultez Considérations sur la [programmation du pilote Callout](/windows-hardware/drivers/network/callout-driver-programming-considerations) dans le kit de pilotes Windows (WDK).

-   Tenez compte des implications en termes de performances lors de l’utilisation de filtres complexes.

    À compter de Windows 7 et de Windows Server 2008 R2, les filtres peuvent être créés avec plusieurs conditions qui utilisent la même clé de champ. Cela permet de créer des stratégies complexes avec moins de filtres. Toutefois, ces filtres complexes peuvent entraîner une baisse des performances du moteur de filtre WFP. Une évaluation doit être effectuée pour déterminer si l’utilisation de ces filtres entraîne un effet néfaste sur les performances globales de votre solution.

 

 
