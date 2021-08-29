---
description: Envoi de demandes d’État COPP
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Envoi de demandes d’État COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34407b5bb865167db65957e12121d6ce91f432eb5fcbd679527f657873dc35d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683829"
---
# <a name="sending-copp-status-requests"></a>Envoi de demandes d’État COPP

Pour envoyer une demande d’État COPP (Certified Output Protection Protocol), remplissez une structure [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) avec les données de la demande. Les membres de la structure sont les suivants :

-   **rApp**. Nombre aléatoire 128 bits, typé en tant que GUID. Le même numéro est retourné dans la réponse du pilote. Vous devez allouer le nombre aléatoire sur le tas, puis le copier dans la structure. Cela permet de protéger les attaques lorsque l’attaquant modifie le contenu de la structure [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .
-   **guidStatusRequestID**. GUID qui identifie la demande. Consultez [référence de requête Copp](copp-query-reference.md).
-   **dwSequence**. Numéro de séquence d’État. Incrémentez cette valeur après chaque demande d’État. (Dans la section [lancement d’une session Copp](initiating-a-copp-session.md), cette valeur est affichée en tant que *uStatusSeq* dans les exemples de code.)
-   **cbSizeData**. Taille, en octets, de toutes les données supplémentaires nécessaires pour la demande.
-   **StatusData**. Données pour la demande d’État.

Transmettez la structure [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) à la méthode [**IAMCertifiedOutputProtection ::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) . Par exemple, le code suivant envoie une demande d’État qui interroge les mécanismes de protection disponibles :


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



La réponse est écrite dans le membre **COPPStatus** de la structure [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) . La taille des données valides dans la réponse est donnée dans le membre **cbSizeData** . Pour garantir l’intégrité du message, le pilote calcule un code d’authentification de message (MAC) à l’aide de l’algorithme OMAC 1 et retourne cette valeur dans le membre **macKDI** de la structure. L’application doit vérifier cette valeur comme suit :

1.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **macKDI** de la structure [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (en d’autres termes, **cbSizeData** plus **COPPStatus**).
2.  Comparez cette balise à la valeur dans **macKDI**, à l’aide d’un **memcmp** simple.

L’algorithme OMAC 1 est décrit en détail dans [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) . COPP utilise les paramètres OMAC-1 suivants :

-   E = AES
-   t = 128 bits

Les données retournées par la demande Status commencent toujours par deux éléments :

-   La même valeur de **rApp** qui a été passée par l’application. Vous devez vérifier que cette valeur correspond à la valeur d’origine stockée sur le tas.
-   Valeur [**de \_ StatusFlags Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) qui indique si l’état de protection de sortie a changé.

Étant donné que la connexion peut être perdue ou reconfigurée, l’application doit régulièrement interroger le pilote pour connaître l’état actuel. Si l' \_ indicateur Copp RenegotiationRequired est défini, l’application doit tenter de réinitialiser le niveau de protection. Si l' \_ indicateur Copp LinkLost est défini, l’application doit arrêter la diffusion du contenu. Par exemple, l' \_ indicateur Copp LinkLost peut être retourné parce que l’utilisateur a déconnecté le connecteur de sortie. L’application doit libérer l’instance actuelle de VMR, créer une nouvelle instance de VMR et établir une nouvelle session COPP (y compris l’échange de clés et la validation de certificat).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



