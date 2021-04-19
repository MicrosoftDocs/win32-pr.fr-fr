---
description: Le filtre d’adresse notifie au pilote Moniteur réseau d’accepter des frames ayant l’un des différents types d’adresses MAC spécifiés (Ethernet, Token Ring et FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Écriture de la partie de filtre ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522194"
---
# <a name="writing-addresstable-filter-portion"></a>Écriture de la partie de filtre ADDRESSTABLE

Le filtre d’adresse notifie au pilote Moniteur réseau d’accepter des frames ayant l’un des différents types d’adresses MAC spécifiés (Ethernet, Token Ring et FDDI). Vous pouvez spécifier un maximum de huit paires d’adresses. Une paire d’adresses peut spécifier une source, une destination, les deux ou aucune des deux.

La partie adresse du filtre est composée de deux structures : [**ADDRESSTABLE**](addresstable.md) et [**ADDRESSPAIR**](addresspair.md).

Si vous ne spécifiez aucune adresse, tous les frames transmettent le filtre d’adresse. Toutefois, si vous spécifiez des adresses, seuls les frames qui passent le filtre d’adresse donné seront transmis.

La génération du filtre d’adresses implique l’allocation d’une structure [**ADDRESSTABLE**](addresstable.md) et le remplissage des membres de la structure [**ADDRESSPAIR**](addresspair.md) .

**Pour générer la partie adresse d’un filtre de capture**

1.  Utilisez l’indicateur **capturefilter \_ indicateurs \_ locaux \_ uniquement** de la structure [**capturefilter**](capturefilter.md) pour limiter la capture au trafic vers et depuis votre ordinateur local.

    La définition de cet indicateur ne définit pas la carte réseau en mode promiscuité. le fichier de capture capture uniquement le trafic local.

2.  Utilisez l’exemple de code suivant pour définir la structure [**ADDRESSTABLE**](addresstable.md) :

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  Utilisez les informations indiquées dans le tableau ci-dessous pour sélectionner un type d’indicateur [**ADDRESSPAIR**](addresspair.md) . 

    | Indicateur                             | Signification                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | indicateurs d’adresse \_ \_ correspondant à l' \_ heure d’été       | Correspond à une adresse de destination.                                                        |
    | indicateurs d’adresse \_ \_ correspondant à \_ src       | Correspond à une adresse source                                                              |
    | indicateurs d’adresse- \_ \_ exclure          | Exclut le frame si cette adresse est trouvée (une source ou une destination définie). |
    | \_identificateurs d’adresse \_ ADR du \_ groupe DST \_ | Correspond au bit de groupe (de l’adresse de destination) uniquement pour les messages de type diffusion.      |
    | \_les indicateurs d’adresse \_ correspondent à la \_ fois      | Correspond à la fois à l’adresse de destination et à la source.                                    |

    

     

4.  Renseignez une adresse de destination, qui est évaluée par rapport à l’indicateur [**ADDRESSPAIR**](addresspair.md) que vous sélectionnez.
5.  Renseignez une adresse source, qui est évaluée par rapport à l’indicateur [**ADDRESSPAIR**](addresspair.md) que vous sélectionnez.
6.  Remplissez la structure [**ADDRESSTABLE**](addresstable.md) avec un tableau de structures [**ADDRESSPAIR**](addresspair.md) , qui comprend les paires d’adresses évaluées par le pilote. Toutes les paires d’adresses sont évaluées comme une instruction OR logique (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Vous pouvez inclure un maximum de huit paires d’adresses dans un filtre de capture.

 

 



