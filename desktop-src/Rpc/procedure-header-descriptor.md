---
title: Descripteur d’en-tête de procédure
description: L’en-tête a été étendu plusieurs fois pendant la durée de vie du moteur de NDR. Le compilateur actuel génère toujours des en-têtes différents en fonction du mode du compilateur. Toutefois, les en-têtes plus récents sont un sur-ensemble des plus anciens.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463538"
---
# <a name="procedure-header-descriptor"></a>Descripteur d’en-tête de procédure

L’en-tête a été étendu plusieurs fois pendant la durée de vie du moteur de NDR. Le compilateur actuel génère toujours des en-têtes différents en fonction du mode du compilateur. Toutefois, les en-têtes plus récents sont un sur-ensemble des plus anciens.

## <a name="the-old-oi-header"></a>L’ancien en-tête-OI

L’en-tête a le format suivant :

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Où le \_ type de handle<1> peut être l’une des valeurs indiquées dans le tableau suivant.



| Hex | Handle               |
|-----|----------------------|
| 31  | \_générique de liaison FC \_    |
| 32  | \_primitive de liaison FC \_  |
| 33  | \_descripteur automatique FC \_     |
| 34  | \_handle de rappel FC \_ |
| 0   | (handle explicite)    |



 

Si le type de handle \_<1> champ est différent de zéro, la procédure utilise alors un handle implicite du type indiqué. Pour plus d’informations, consultez la rubrique [Handles](handles.md) . Si le type de handle \_<1> champ est égal à zéro, le handle utilisé pour la liaison est l’un des paramètres de la procédure.

Les handles explicites peuvent être de la primitive, du générique et du contexte. la dernière a le jeton FC suivant.



| Hex | Handle            |
|-----|-------------------|
| 30  | \_contexte de liaison FC \_ |



 

Par Convention, le type de handle pour les interfaces DCOM est le \_ \_ descripteur auto FC.

Les \_ indicateurs Oi<1> champ est un masque de 8 bits des indicateurs suivants.



| Hex | Indicateur                         | Signification                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Point de \_ pointeur complet de OI \_ \_ utilisé          | Utilise le package de pointeurs complet.           |
| 02  | OI \_ RPCSS \_ RPCSS \_ utilisé       | Utilise le package de mémoire RpcSs.           |
| 04  | Procédure de l' \_ objet OI \_             | Procédure dans une interface d’objet.      |
| 08  | OI \_ a \_ RPCFLAGS            | La procédure a des indicateurs RPC non nuls.     |
| 10  | OI\_\*                       | Surchargé.                              |
| 20  | OI\_\*                       | Surchargé.                              |
| 40  | OI \_ utiliser \_ de \_ nouvelles \_ routines init | Utilise les routines init et Windows NT 3.5 bêta 2. |
| 80  |                              | Inutilisé.                                  |



 

Les indicateurs suivants sont surchargés.



| Hex | Indicateur                                    | Signification                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | ENCODE \_ est \_ utilisé                        | Utilisé uniquement dans le choix.                              |
| 20  | le décodage \_ est \_ utilisé                        | Utilisé uniquement dans le choix.                              |
| 10  | OI \_ Ignorer \_ la \_ gestion des exceptions d’objets \_ | N’est plus utilisé (anciennement OLE).                         |
| 20  | OI \_ a \_ comm \_ ou \_ Fault                | Dans le protocole RPC brut uniquement, \[ comm \_ , état d’erreur \_ \] .        |
| 20  | OI \_ obj \_ use \_ v2 \_ interpréteur           | Dans DCOM uniquement, utilisez l’interpréteur d' [**interfaces**](/windows/desktop/Midl/-oi) de protocole. |



 

Le \_ champ indicateurs rpc<4> décrit comment définir le champ **RpcFlags** de la structure [**de \_ message RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) . Ce champ est présent uniquement si les \_ indicateurs oi<1> champ contient la \_ valeur de \_ RPCFLAGS définie. Si ce champ n’est pas présent, les indicateurs RPC de la procédure distante sont nuls.

> [!Note]  
> Pour des performances, les interpréteurs Async ont toujours le \_ champ indicateurs rpc<4> présent.

 

Le \_ champ proc num<2> indique le numéro de procédure de la procédure.

La \_ taille de la pile<2> fournit la taille totale de tous les paramètres sur la pile, y compris ce pointeur et/ou la valeur de retour.

Le \_ champ Description du handle explicite \_<> est décrit plus loin dans ce document. Ce champ n’est pas présent si la procédure utilise un handle implicite.

 

 