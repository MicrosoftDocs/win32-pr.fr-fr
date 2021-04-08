---
description: Les informations principales fournies par une application pour initier une session de communication sont le type d’adresse, le type de média ou les types, ainsi que l’adresse de destination.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Initier une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e925ba90460b88c85a9aab1624923acdbc4572a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863857"
---
# <a name="initiate-a-session"></a>Initier une session

Les informations principales fournies par une application pour initier une session de communication sont le [type d’adresse](address-type-ovr.md), le type de [média](media-type-ovr.md) ou les types, ainsi que l' [adresse](address-ovr.md)de destination.

L’adresse de destination peut nécessiter une [traduction d’adresse](#address-translation) pour placer les informations entrées par un utilisateur dans le format approprié pour un type d’adresse donné. Par exemple, un numéro de téléphone qui se trouvait dans un carnet d’adresses électronique au format [canonique](address-ovr.md) nécessitera [un format de](address-ovr.md) traduction.

Certaines sessions peuvent nécessiter des paramètres d’installation spéciaux, s’ils sont pris en charge par le fournisseur de services. Par exemple, un TSP RNIS peut transmettre des informations sur l’utilisateur, et certains MSP requièrent des informations sur la direction du flux de média. Consultez les [informations de session](session-information-ovr.md) pour consulter les données qui peuvent être définies ou obtenues concernant une session.

Une fois qu’une session a été lancée, l’interface TAPI informe l’application de la progression de l’appel à l’aide du mécanisme de notification d’événements configuré pendant l’initialisation.

**TAPI 2. x :** Les applications initient une session à l’aide de la fonction [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) . La fonction [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) est utilisée pour effectuer la traduction d’adresses, si nécessaire.

Les paramètres d’appel peuvent être stockés dans la structure de données [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) , et un pointeur vers cette structure est ensuite utilisé en tant que paramètre de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall). Si aucune structure **LINECALLPARAMS** n’est fournie à **lineMakeCall**, un appel de niveau vocal par défaut est demandé avec un ensemble de valeurs par défaut.

Si la session est correctement configurée, un descripteur d’appel avec [des privilèges](privilege-ovr.md) de *propriétaire* est renvoyé à l’application et TAPI envoie la ligne d’application [**\_ CALLSTATE**](./line-callstate.md) des messages avec les informations relatives à la progression de l’appel. Les applications utilisent généralement ces messages pour afficher les rapports d’État à l’utilisateur.

**TAPI 3. x :** Les applications initient une session de communication en appelant la méthode [**ITAddress :: createCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) sur une adresse qui gère le type d’adresse et le type de média requis. Si l’adresse expose l’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) , les terminaux sont sélectionnés sur les flux de médias de l’objet d’appel. Pour obtenir une illustration de ce processus, consultez l’exemple de code [Make a Call](make-a-call.md) .

Les paramètres d’appel peuvent être stockés ou modifiés à l’aide des méthodes exposées par l’interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

Si la session est correctement configurée, TAPI retourne un pointeur d’interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) qui peut être utilisé pour d’autres opérations de session, ou pour obtenir un pointeur d’interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) qui peut être utilisé pour acquérir des informations de session supplémentaires. L’interface [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) traite les événements d’état d’appel TAPI.

> [!Note]  
> L’interface TAPI ne doit pas être utilisée pour les transmissions de télécopie. Utilisez plutôt les fonctions disponibles via MAPI, l’API de messagerie Microsoft.

 

## <a name="address-translation"></a>Traduction d’adresses

Une application d’utilisateur final ou de serveur peut stocker des adresses dans un format qui n’est pas compatible avec les besoins d’un fournisseur de services donné. Par exemple, un numéro de téléphone peut être stocké dans un carnet d’adresses électronique au [format canonique](address-ovr.md), mais la plupart des fournisseurs de services qui gèrent les numéros de téléphone requièrent le [format de numérotation](address-ovr.md).

L’interface TAPI fournit des opérations de traduction d’adresses qui aident une application à présenter le type d’adresse correct à un TSP. Le fournisseur de services spécifie à TAPI les types d’adresses qu’il prend en charge et n’a pas besoin d’inclure une forme de traduction d’adresse.

**TAPI 2. x :** Consultez [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3 :** Consultez [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Listes de péage

À certains emplacements de Amérique du Nord, tous les appels téléphoniques placés dans le code de la zone locale sont des appels locaux. Dans d’autres emplacements, certains appels placés dans le code de la zone locale sont de longue distance et ont besoin d’un préfixe « 1 » à composer. Les trois premiers chiffres de l’adresse (le préfixe) déterminent si un appel dans le code de la zone locale est un appel payant.

Une *liste de numéros de téléphone* est une liste de préfixes dans le code de la zone locale dont les adresses doivent être numérotées en tant qu’adresses longues et sont facturées à long terme.

Les listes de péages ne sont pas pertinentes pour les fournisseurs de services ou pour les applications qui n’accèdent pas à un réseau téléphonique.

**TAPI 2. x :** Consultez [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ INTOLLLIST et LINETRANSLATERESULT \_ NOTINTOLLLIST bits dans la structure [**LINETRANSLATEOUTPUT**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) ), [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3 :** Consultez [**ITAddressTranslation :: TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo :: obtenir \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
