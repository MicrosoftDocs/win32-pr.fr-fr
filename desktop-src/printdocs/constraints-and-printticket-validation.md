---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Validation des contraintes et PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddcc1f6f3ad496b6bfb6ed201cf93c2b4a10679
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953492"
---
# <a name="constraints-and-printticket-validation"></a>Validation des contraintes et PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Comme indiqué dans la section schéma PrintCapabilities, certains des résultats de configuration possibles exprimés dans un document PrintCapabilities ne sont pas valides pour l’appareil. Les configurations non valides sont dites qu’elles contiennent des conflits de contrainte (terme utilisé dans le monde des fichiers PPD/GPD). Afin d’éviter les conflits de contraintes, les fournisseurs PrintTicket doivent prendre en charge une opération de validation PrintTicket que les clients utilisent pour effectuer la validation sur leur PrintTicket. Cette opération doit détecter si la configuration spécifiée peut se produire sur l’appareil. Si la configuration ne peut pas se produire (car les éléments de fonctionnalité et d’option spécifiés n’existent pas dans l’appareil actuel, ou parce que la configuration est contrainte), l’opération doit modifier le PrintTicket d’entrée pour qu’il contienne des paramètres valides et non restreints. L’opération peut également supprimer ou valider d’autres informations dans PrintTicket. Notez que lorsqu’un conflit de contrainte se produit, le code de validation doit modifier le paramètre de l’un des attributs de l’appareil afin d’éviter le conflit de contrainte. Les [définitions d’option](option-definitions.md) suggèrent qu’un processus de calcul de score défini pour le pilote de périphérique doit être utilisé pour déterminer l’attribut d’appareil qui doit être modifié afin de préserver au mieux l’intention initiale de l’utilisateur. Le code de validation peut coder en dur le processus de notation pour préférer un attribut d’appareil sur un autre, ou il peut utiliser les informations fournies par une instance de propriété particulière dans PrintTicket pour guider la résolution. Étant donné qu’aucune propriété n’est définie dans les mots clés de schéma d’impression qui permet aux clients de spécifier la priorité relative de chaque attribut d’appareil, tous les éléments de propriété PrintTicket privés utilisés à cet effet sont susceptibles d’être ignorés par d’autres fournisseurs PrintTicket.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



