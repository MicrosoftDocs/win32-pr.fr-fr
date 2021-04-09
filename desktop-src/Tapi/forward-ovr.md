---
description: Le transfert est le détournement d’une session entrante vers une adresse de destination différente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Transférer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862618"
---
# <a name="forward"></a>Transférer

Le transfert est le détournement d’une session entrante vers une adresse de destination différente. L’interface TAPI permet à une application de spécifier une liste de conditions de transfert pour une adresse. Les conditions de transfert peuvent être aussi finement grainées qu’une destination et un [**mode de transfert**](./lineforwardmode--constants.md) différents pour chaque adresse d’appelant.

L’opération de transfert peut également être utilisée pour implémenter une fonctionnalité de do-not-sélective, en transférant certains appelants vers la messagerie vocale et en permettant à d’autres utilisateurs de tenter de se terminer.

L’opération de transfert peut également annuler tout transfert actuellement en vigueur.

Certains fournisseurs de services requièrent qu’une application crée un appel de consultation avant une opération de transfert. Un pointeur désignant l’appel de consultation est ensuite passé à l’opération de transfert.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Pour définir [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) sur [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), modifiez la [**ligne \_ ADDRESSSTATE**](./line-addressstate.md) message de notification avec LINEADDRESSSTATE \_ Forward.

**TAPI 3. x :** Consultez [**ITAddress :: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress :: obtenir \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification : [**ITAddressEvent :: obtenir un \_ événement**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) avec AE \_ Forward.

> [!Note]  
> Il peut être impossible pour un fournisseur de services de savoir à tout moment quel transfert est en vigueur pour une adresse. Le transfert peut être annulé ou modifié de manière à ne pas envoyer de notification au fournisseur de services.

 

 

 
