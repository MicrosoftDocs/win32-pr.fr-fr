---
description: Les données protégées sont stockées sous la forme d’un objet BLOB encodé ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Format de données protégées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907404"
---
# <a name="protected-data-format"></a>Format de données protégées

Les données protégées sont stockées sous la forme d’un objet BLOB encodé ASN. 1. Les données sont mises en forme en tant que contenu associé à CMS (Certificate Message Syntax). L’enveloppe numérique contient du contenu chiffré, des informations de destinataire qui contiennent une clé de chiffrement de contenu chiffrée (clé CEK) et un en-tête qui contient des informations sur le contenu, y compris la chaîne de règle du descripteur de protection non chiffré. Cela est illustré par le diagramme suivant.

![données enveloppées protégées](images/protecteddatablob.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[Descripteurs de protection](protection-descriptors.md)
</dt> <dt>

[Fournisseurs de protection](protection-providers.md)
</dt> </dl>

 

 



