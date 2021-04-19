---
description: L’exemple de code suivant illustre l’utilisation de l’objet TAPI pour examiner les ressources de téléphonie disponibles pour une adresse qui peut gérer un ensemble spécifié de spécifications de type de média. Dans cet exemple, l’audio et la vidéo sont les médias requis.
ms.assetid: 8be40a87-931d-4cda-9ef7-f9c0489e0b7b
title: Sélectionner une adresse
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: da41059c38328ff00271e4fa561561eecf83e1cb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106537300"
---
# <a name="select-an-address"></a>Sélectionner une adresse

L’exemple de code suivant illustre l’utilisation de l’objet TAPI pour examiner les ressources de téléphonie disponibles pour une adresse qui peut gérer un ensemble spécifié de spécifications de type de média. Dans cet exemple, l’audio et la vidéo sont les médias requis.

Avant d’utiliser cet exemple de code, vous devez effectuer les opérations dans [initialiser l’interface TAPI](initialize-tapi.md).

> [!NOTE]  
> Cet exemple ne dispose pas de la vérification des erreurs et des versions appropriées pour le code de production.

```cpp
// Declare the interfaces used to select an address.
IEnumAddress * pIEnumAddress;
ITAddress * pAddress;
ITMediaSupport * pMediaSupport;

// Use the TAPI object to enumerate available addresses.
hr = gpTapi->EnumerateAddresses( &pIEnumAddress );
// If (hr != S_OK) process the error here. 

// Locate an address that can support the media type the application needs.
while ( S_OK == pIEnumAddress->Next(1, &pAddress, NULL) )
{
    // Determine the media support.
    hr = pAddress->QueryInterface(
         IID_ITMediaSupport,
         (void **)&pMediaSupport
         );
    // If (hr != S_OK) process the error here. 

    // In this example, the required media type is already known.
    // The application can also use the address object to
    // enumerate the media supported, then choose from there.
    hr = pMediaSupport->QueryMediaType(
         TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
         &bSupport
         );
    // If (hr != S_OK) process the error here. 

    if (bSupport)
    {
        break;
    }
}
// pAddress is now a usable address.
```

## <a name="related-topics"></a>Rubriques connexes

[ITTAPI::EnumerateAddresses](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[ITMediaSupport](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[\_Constantes TAPIMEDIATYPE](tapimediatype--constants.md)
