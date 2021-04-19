---
description: Explique comment valider manuellement les informations d’identification Schannel.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Validation manuelle des informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521882"
---
# <a name="manually-validating-schannel-credentials"></a>Validation manuelle des informations d’identification Schannel

Par défaut, Schannel valide le [*certificat de serveur*](../secgloss/s-gly.md) en appelant la fonction [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ; Toutefois, si vous avez désactivé cette fonctionnalité à l’aide de l' \_ \_ indicateur de \_ \_ validation d’identification manuelle d’ISC req, vous devez valider le certificat fourni par le serveur qui tente d’établir son identité.

Pour valider manuellement le certificat de serveur, vous devez d’abord l’extraire. Utilisez la fonction [**QueryContextAttributes (général)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) et spécifiez la \_ valeur de l’attribut de \_ contexte certificat distant attr SECPKG \_ \_ . Cet attribut retourne une structure de [**\_ contexte de certificat**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) contenant le certificat fourni par le serveur. Ce certificat est appelé le certificat feuille, car il s’agit du dernier certificat dans la chaîne de certificats et il est le plus éloigné du [*certificat racine*](../secgloss/r-gly.md).

À l’aide du certificat feuille, vous devez vérifier les éléments suivants :

-   La chaîne de certificats est terminée et la racine est un certificat d’une [*autorité de certification*](../secgloss/c-gly.md) approuvée.
-   L’heure actuelle n’est pas postérieure aux dates de début et de fin de chacun des certificats de la chaîne de certificats.
-   Aucun des certificats de la chaîne de certificats n’a été révoqué.
-   La profondeur du certificat feuille n’est pas plus profonde que la profondeur maximale autorisée spécifiée dans l’extension de certificat. Cette vérification n’est nécessaire que si une profondeur est spécifiée.
-   L’utilisation du certificat est correcte, par exemple, un [*certificat client*](../secgloss/c-gly.md) ne doit pas être utilisé pour authentifier un serveur.
-   Pour l’authentification du serveur, l’identité du serveur contenue dans le certificat feuille du serveur correspond au serveur que le client tente de contacter. En règle générale, le client met en correspondance un élément dans le champ nom d’objet du certificat avec l’adresse IP ou le nom DNS du serveur.

 

 
