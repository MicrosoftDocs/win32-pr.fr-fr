---
description: La communication implique souvent des quantités potentiellement volumineuses de données ou de données de longueur inconnue.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Utilisation de SecBufferDesc et SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca7d8155a610263838d2baf2a7d1c8fc96ec874
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096221"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Utilisation de SecBufferDesc et SecBuffer

La communication implique souvent des quantités potentiellement volumineuses de données ou de données de longueur inconnue. L’envoi et la réception de données s’effectuent de manière similaire ou identique dans les deux cas. Pour traiter une longueur inconnue et potentiellement de grandes quantités de données, la communication SSPI s’effectue à l’aide de deux structures, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) et [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Une structure [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) est un conteneur pour un tableau de structures [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) . Une structure **SecBufferDesc** contient les membres suivants :

-   Numéro de version
-   Nombre d’éléments [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Adresse du tableau de structures [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Une structure [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contient les trois membres suivants :

-   Nombre d’octets dans la mémoire tampon
-   Type d’informations contenues dans l’élément de données
-   Octets eux-mêmes

Un message SSPI entier se compose souvent d’un tableau de structures [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) .

Les types de données de mémoire tampon suivants sont définis comme suit.



| Type de mémoire tampon                | Signification                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ vide           | Non défini, remplacé par la fonction de [*package de sécurité*](../secgloss/s-gly.md) |
| \_données SECBUFFER            | Données du paquet                                                                                                                            |
| \_jeton SECBUFFER           | Jeton de sécurité                                                                                                                         |
| \_paramètres SECBUFFER pkg \_     | Paramètres spécifiques au package                                                                                                            |
| SECBUFFER \_ manquant         | Indicateur de données manquant                                                                                                                 |
| SECBUFFER \_ extra           | Données supplémentaires                                                                                                                             |
| \_flux SECBUFFER          | Données de flux de sécurité                                                                                                                   |
| Code de fin de \_ flux SECBUFFER \_ | Code de fin de flux de sécurité                                                                                                                |
| \_ \_ en-tête de flux SECBUFFER  | En-tête de flux de sécurité                                                                                                                 |



 

Les types de tampons ci-dessus peuvent être combinés à l’aide d'**une opération or au niveau** du bit avec l’un des types de mémoires tampons suivants.



| Type de mémoire tampon         | Signification                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Masquez les attributs de sécurité en séparant les indicateurs d’attribut du type de mémoire tampon. |
| SECBUFFER en \_ lecture seule | La mémoire tampon est en lecture seule                                                              |



 

Avant chaque appel à une API SSPI qui requiert un paramètre [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) , un ou plusieurs éléments de tableau [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) sont déclarés et initialisés. Par exemple, il peut y avoir deux mémoires tampons de sécurité : une qui contient les données de message d’entrée et l’autre pour le jeton de sécurité opaque de sortie retourné par le package de sécurité. L’ordre des tampons de sécurité dans le descripteur de mémoire tampon de sécurité n’est pas important, mais chaque mémoire tampon doit être marquée avec le type approprié. Une balise en lecture seule peut être utilisée avec n’importe quelle mémoire tampon d’entrée qui ne doit pas être modifiée par le [*package de sécurité*](../secgloss/s-gly.md).

La taille de la mémoire tampon de sortie supposée contenir le jeton de sécurité est importante. Une application peut trouver la taille de jeton maximale pour un package de sécurité lors de l’installation initiale. L’appel à [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) retourne un tableau de pointeurs vers les informations de package de sécurité. La structure d’informations du package de sécurité contient la taille de jeton maximale pour chaque package. Dans l’exemple, les informations se trouvent dans le membre **cbMaxToken** de la structure [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . Les mêmes informations peuvent être obtenues ultérieurement à l’aide de [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

L’application initialise les pointeurs et les tailles de tampon dans la description de la mémoire tampon pour indiquer l’emplacement des données de message et d’autres informations.

Pour plus d’informations, consultez [exemple de code SecBuffer et SecBufferDesc](secbuffer-and-secbufferdesc-example-code.md).

 

 
