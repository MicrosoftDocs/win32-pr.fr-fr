---
description: Les opérations de numérotation permettent à une application d’envoyer des chiffres supplémentaires sur une session créée précédemment. Un exemple d’utilisation de la numérotation partielle consiste à composer une extension. La numérotation partielle est parfois appelée numérotation incrémentielle ou numérotation retardée.
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: Composer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750780"
---
# <a name="dial"></a>Composer

Les opérations de numérotation permettent à une application d’envoyer des chiffres supplémentaires sur une session créée précédemment. Un exemple d’utilisation de la numérotation partielle consiste à composer une extension. La numérotation partielle est parfois appelée numérotation incrémentielle ou numérotation retardée.

Lorsque l’adresse fournie est incomplète, la composition de certains des chiffres peut être retardée en plaçant un point-virgule (;) à la fin du nombre. Une opération de numérotation est ensuite utilisée pour envoyer des données d’adresse supplémentaires sur la session existante, telles que la numérotation de l’adresse d’un tiers vers lequel l’appel sera transféré.

Chaque fournisseur de services doit rejeter une chaîne de numérotation qui contient le **?** et laissez l’application s’en occuper, le cas échéant. Par exemple, l’application peut utiliser la numérotation partielle pour composer la chaîne, jusqu’à, mais n’inclut pas le **?** , puis affiche une boîte de dialogue qui permet à l’utilisateur de signaler quand le reste de la chaîne de numérotation doit être composé.

Une autre raison pour laquelle une application d’utiliser la numérotation partielle est que le fournisseur de services ne prend pas en charge un ou plusieurs des caractères de contrôle de la détection de progression des appels. Ces caractères, qui peuvent se produire dans une adresse de numérotation, sont W (attendre la tonalité); @ (attendre une réponse silencieuse); et $ (attendre la tonalité d’invite de la carte d’appel). Ces caractères et tous les autres caractères utilisés dans les chaînes d’adresses sont décrits plus en détail dans la section [adresses de numérotation](address-ovr.md).

Le fournisseur indique les modificateurs de chaîne de numérotation qu’il prend en charge. Une application TAPI 2 trouve ces données dans le membre **dwDevCapFlags** de la structure [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) retournée par [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps). Une application TAPI 3 appelle [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) avec *AddressCap* défini sur le membre **AC \_ DEVCAPFLAGS** de [**la \_ fonctionnalité Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

L’application peut choisir de préanalyser les chaînes de numérotation pour les caractères non pris en charge ou elle peut transmettre la chaîne « brute » dans le cadre de l’initialisation d’une session. Si la chaîne contient un modificateur non pris en charge ou un «  ? », le fournisseur retourne une erreur indiquant quel modificateur incriminé s’est produit en premier dans la chaîne :

-   LINEERR \_ DIALBILLING
-   LINEERR \_ DIALQUIET
-   LINEERR \_ DIALDIALTONE
-   LINEERR \_ DIALPROMPT

L’application peut ensuite localiser le modificateur incriminé dans la chaîne, prendre les chiffres à gauche du modificateur, ajouter un point-virgule et initialiser une session à l’aide de l’adresse partielle. Le reste de la chaîne peut être envoyé à l’aide de l’opération de numérotation.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial).

**TAPI 3. x :** Consultez [**ITBasicCallControl ::D tial**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial).

 

 
