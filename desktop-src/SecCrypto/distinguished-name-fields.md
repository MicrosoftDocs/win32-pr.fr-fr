---
description: Contient des informations qui doivent identifier de façon unique la personne qui effectue la demande.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Champs de noms uniques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10465a481c1efbaa9637979bb5bb82880451fbe43800b968a4c9fefc5fbc4a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767264"
---
# <a name="distinguished-name-fields"></a>Champs de noms uniques

Une [*demande de certificat*](../secgloss/c-gly.md) contient des informations qui doivent identifier de façon unique la personne qui effectue la demande.

Les \# demandes de certificat au format PKCS 10 acceptées par les services de certificats contiennent des champs d’identification appelés champs nom unique (DN). Ces champs contiennent les informations entrées par l’utilisateur lors de la création d’une demande de certificat par le gestionnaire de clés, [le contrôle d’inscription de certificat](certificate-enrollment-control.md)ou d’autres moyens.

Voici quelques indications sur l’achèvement des champs DN dans une demande de certificat.



| Champ               | Description                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom commun         | Certificats d’utilisateur : vous devez entrer le nom complet de la personne. Certificats d’ordinateur : vous devez entrer le ***/** _chemin d’accès_ complet * du nom d’hôte utilisé dans les recherches DNS sur lesquelles le serveur s’exécutera (par exemple, *hostname ***.** _Exemple_* _. com_*).<br/>                                                                                                  |
| Organisation        | Le nom que vous spécifiez pour le champ organisation doit être le nom légal de votre organisation inscrit auprès de la ville, de l’État ou de l’autorité de pays/région. Le nom légal de l’organisation doit être utilisé dans le champ organisation.                                                                                                      |
| Organizational Unit (Unité d’organisation) | Le champ unité d’organisation peut être utilisé pour différencier les différentes divisions au sein d’une organisation, par exemple « unité de sécurité Internet » ou « ressources humaines ». Il est également recommandé d’utiliser ce champ pour spécifier une valeur DBA (en cours de...).                                                                                           |
| Localité            | Le champ localité indique la ville dans laquelle l’organisation réside. Si l’organisation ne dispose que d’une licence locale, en raison de la présence d’une licence commerciale enregistrée auprès du régisseur City pour la ville de Cambridge dans l’état du Massachusetts, le champ Locality doit contenir Cambridge.                                                                |
| State or Province   | Le champ État ou province spécifie l’emplacement physique de l’organisation. Si votre organisation est incorporée au Delaware mais a un administrateur de bases de l’entreprise (en cours de...) en Californie, utilisez California. Le champ État ou province ne doit pas être un champ abrégé. Par exemple, « CA » n’est pas un nom d’état valide. « California » est le nom d’état approprié. |
| Pays/région      | Le modèle de nommage [*X. 500*](../secgloss/x-gly.md) standard requiert un code de pays/région à 2 caractères. Le code de pays/région pour le États-Unis est US ; le code pays/région pour le Canada est CA.                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du nom](name-properties.md)
</dt> </dl>

 

 
