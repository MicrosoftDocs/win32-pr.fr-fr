---
description: Les services de certificats prennent en charge l’utilisation de certificats tels que définis dans la recommandation ITU-T X. 509 (également ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propriétés du certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864362"
---
# <a name="certificate-properties"></a>Propriétés du certificat

Les services de certificats prennent en charge l’utilisation de certificats tels que définis dans la recommandation ITU-T [*X. 509*](../secgloss/x-gly.md) (également ISO/IEC 9594-8). Voici les propriétés contenues dans un certificat X. 509 standard.



| Champ                                       | Description                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version                                     | Numéro de version du format du certificat.                                                                                                                                                                       |
| Numéro de série                               | Numéro de série du certificat. Ce nombre est attribué par l’émetteur et est unique dans la liste des certificats émis de l’émetteur.                                                                          |
| Identificateurs et paramètres d’algorithme         | Algorithme de signature et tous les paramètres utilisés par l’émetteur.                                                                                                                                                      |
| Émetteur                                      | Nom de l' [*autorité de certification*](../secgloss/c-gly.md) qui a émis le certificat.                                               |
| Pas avant (date)                           | Le certificat n’est pas valide avant cette date.                                                                                                                                                                         |
| Pas après (date)                            | Le certificat n’est pas valide après cette date.                                                                                                                                                                          |
| Nom de sujet                                | Nom de la personne ou de l’entité à qui le certificat est émis. Ce champ peut également inclure l’organisation, l’unité d’organisation, la localité, l’État ou la région, le pays ou la région du destinataire du certificat. |
| Algorithme de clé publique de l’objet et paramètres | L’algorithme et les paramètres utilisés pour la [*clé publique*](../secgloss/p-gly.md)du sujet.                                                                       |
| Clé publique de l’objet                          | Clé publique réelle (une chaîne de bits).                                                                                                                                                                           |
| Signature                                   | Signature fournie par l’émetteur.                                                                                                                                                                            |



 

Un certificat peut contenir les éléments suivants, en fonction de la version [*X. 509*](../secgloss/x-gly.md) du certificat.



| Champ facultatif    | Description                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID unique de l’émetteur  | Utilisé pour rendre le nom de l’émetteur non ambigu s’il a été utilisé par plusieurs entités. Présent uniquement dans les versions [*X. 509*](../secgloss/x-gly.md) 2,0 ou ultérieures.<br/> |
| ID unique de l’objet | Permet de rendre le nom de l’objet non ambigu s’il a été utilisé par plusieurs entités. Présent uniquement dans X. 509 2,0 ou version ultérieure.<br/>                                                                     |
| Extensions        | Pour spécifier les propriétés personnalisées souhaitées. N’importe quel nombre de champs d’extension peut être inclus dans le certificat. Présent uniquement dans la version X. 509 3,0.<br/>                                            |



 

> [!Note]  
> Les services de certificats Microsoft délivrent des certificats X. 509 version 3.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du nom](name-properties.md)
</dt> </dl>

 

 
