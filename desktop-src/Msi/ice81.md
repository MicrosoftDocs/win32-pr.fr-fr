---
description: ICE81 valide la table MsiDigitalCertificate, la table MsiDigitalSignature, la table MsiPatchCertificate et la table MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021480"
---
# <a name="ice81"></a>ICE81

ICE81 valide la table [MsiDigitalCertificate](msidigitalcertificate-table.md), la table [MsiDigitalSignature](msidigitalsignature-table.md), la table [MsiPatchCertificate](msipatchcertificate-table.md)et la [table MsiPackageCertificate](msipackagecertificate-table.md). Cette action personnalisée ICE publie des avertissements pour les certificats numériques qui sont inutilisés ou non référencés, et publie une erreur lorsque l’objet signé n’existe pas ou lorsque le cabinet de l’objet signé ne pointe pas vers des données externes.

Notez que ICE03 vérifie que l’entrée dans la colonne de table de la table MsiDigitalSignature est « Media ».

## <a name="result"></a>Résultats

ICE81 publie les avertissements suivants pour les certificats numériques non utilisés ou non référencés.



| AVERTISSEMENT ICE81                                                                                                                                                      | Description                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Aucune référence à l’un des enregistrements de la table MsiDigitalCertificate n’a été trouvée dans les tables MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate. | Cet avertissement est retourné si tous les enregistrements sont inutilisés.                |
| Aucune référence au certificat numérique \[ 1 \] n’a été trouvée dans les tables MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.                         | Cet avertissement est retourné si certains enregistrements, mais pas tous, ne sont pas utilisés. |



 

ICE81 publie les erreurs suivantes.



| Erreur ICE81                                                                                                                                                              | Description                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La table multimédia n’existe pas. Par conséquent, toutes les entrées dans MsiDigitalSignature sont incorrectes                                                                                   | L’objet signé n’existe pas. Cette erreur est retournée si la table de média n’existe pas mais que MsiDigitalSignature a des entrées.                                |
| Objet signé manquant \[ 2 \] dans la table multimédia                                                                                                                               | L’objet signé \[ 2 \] n’existe pas. Cette erreur est retournée si la table de supports existe, mais que cette entrée dans MsiDigitalSignature n’est pas présente dans la table des médias. |
| L’entrée dans le tableau \[ 1 \] avec la clé \[ 2 \] est signée. Par conséquent, l’armoire doit pointer vers un objet situé en dehors du package (la valeur du cabinet ne doit pas être préfixée \# ) | Le cabinet de l’objet signé ne pointe pas vers des données externes. \[1 \] est un nom de table. \[2 \] est la clé de la table des médias.                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



