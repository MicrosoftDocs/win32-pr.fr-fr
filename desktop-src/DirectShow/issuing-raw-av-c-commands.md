---
description: Émission de commandes AV/C brutes
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Émission de commandes AV/C brutes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729cad0be3a55a3f95592e54e8f91b9074892a8d111da9ad996b4e00a136cbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153786"
---
# <a name="issuing-raw-avc-commands"></a>Émission de commandes AV/C brutes

Les interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)et [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) fonctionnent en traduisant les appels de méthode en commandes pour le pilote, puis en interprétant la réponse du pilote et en la renvoyant via un **HRESULT** ou un paramètre de sortie. Toutefois, certaines fonctions de l’appareil peuvent ne pas être accessibles par le biais de ces méthodes. Par conséquent, MSDV prend en charge l’envoi de commandes AV/C brutes à l’appareil.

Vous devez garder à l’esprit les points suivants lors de l’utilisation de cette fonctionnalité :

-   La commande est passée directement à l’appareil, sans vérification des erreurs ni validation de paramètre. pour cette raison, vous devez émettre des commandes AV/C brutes uniquement lorsque les interfaces DirectShow n’implémentent pas les fonctionnalités dont vous avez besoin.
-   Toutes les commandes AV/C brutes sont synchrones. Le thread émettant la commande se bloque jusqu’à ce que la commande retourne.
-   Une seule commande peut être donnée à la fois. Pendant le traitement de la commande, l’appareil rejette toutes les commandes supplémentaires.
-   Le pilote UVC ne prend pas en charge les commandes AV/C brutes.

Pour envoyer une commande AV/C, mettez en forme la commande sous la forme d’un tableau d’octets. Appelez ensuite [**IAMExtTransport :: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Transmettez l' \_ indicateur Ed RAW \_ ext \_ dev \_ cmd, la taille du tableau et le tableau. Vous devez effectuer un cast de l’adresse du tableau en un type **LPOLESTR \*** , car l’objectif initial de ce paramètre était de retourner une valeur de chaîne.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR*) AvcCmd);
```



Le contenu du tableau est transmis directement à l’appareil. vous devez donc veiller à le mettre en forme correctement. Une commande peut cibler l’unité (caméscope) ou une sous-unité (bande ou caméra). Les normes pertinentes sont disponibles sur le [site Web 1394 Trade Association](https://1394ta.org).

-   Spécification générale du jeu de commandes de l’interface numérique AV/C
-   Spécification de la sous-unité d’enregistreur/lecteur de bande AV/C

La première décrit comment mettre en forme des commandes AV/C et répertorie les commandes d’unité. La dernière spécification répertorie les commandes de sous-unité.

La méthode **GetTransportBasicParameters** peut retourner l’un des codes d’erreur suivants :



| Code d'erreur              | Description                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| \_délai d’erreur          | La commande a expiré.                                                           |
| ERREUR \_ req \_ non \_ ACCEP  | L’appareil n’a pas accepté la commande.                                           |
| ERREUR \_ non \_ prise en charge   | L’appareil ne prend pas en charge la commande.                                         |
| demande d’erreur \_ \_ abandonnée | La commande a été abandonnée. Possbly l’appareil a été supprimé ou une réinitialisation du bus s’est produite. |



 

> [!Note]  
> Ces erreurs sont retournées sous la forme de codes d’erreur Win32, et non HRESULT. vous devez donc tester ces valeurs directement, plutôt que d’utiliser les macros ayant **réussi** et **échoué** .

 

Si la méthode retourne la valeur \_ OK, la réponse de l’appareil est copiée dans le tableau. La charge utile de la réponse peut être plus grande que la commande. vous devez donc allouer une mémoire tampon suffisamment grande pour la conserver. La taille maximale de la charge utile est de 512 octets. Notez qu’une valeur de retour de S \_ OK ne signifie pas toujours que l’appareil a correctement exécuté la commande. L’application doit examiner la charge utile de réponse pour déterminer l’État.

L’exemple suivant illustre la commande permettant de rechercher une recherche de numéro de piste absolue :


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



