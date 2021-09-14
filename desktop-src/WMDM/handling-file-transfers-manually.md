---
title: Gestion manuelle des transferts de fichiers
description: Gestion manuelle des transferts de fichiers
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Gestionnaire de périphériques de média, transferts de fichiers manuels
- Gestionnaire de périphériques, transferts de fichiers manuels
- Guide de programmation, transferts de fichiers manuels
- applications de bureau, transferts de fichiers manuels
- création d’applications Windows Media Gestionnaire de périphériques, transferts de fichiers manuels
- transferts de fichiers manuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008519"
---
# <a name="handling-file-transfers-manually"></a>Gestion manuelle des transferts de fichiers

Votre application peut implémenter l’interface [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) pour gérer une partie du processus de lecture ou d’écriture. Sur une lecture à partir de l’appareil, l’implémentation permet à l’application de recevoir des blocs de données brutes à partir d’un fichier d’appareil. Sur une écriture sur un appareil, elle permet à l’application d’envoyer des blocs de données brutes à un fichier sur l’appareil.

Dans les opérations de lecture et d’écriture, la méthode [**IWMDMOperation :: TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) passe les données entre l’ordinateur et l’appareil. pour connaître la direction du transfert de données, votre application doit définir un indicateur lorsque Windows Media Gestionnaire de périphériques appelle [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) ou [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite). Lorsque la méthode [**end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) est appelée, l’application doit réinitialiser cet indicateur.

> [!Note]  
> Si le fournisseur de services et l’appareil implémentent correctement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2), il appelle d’abord la méthode [IWMDMOperation3 :: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) de l’application, si elle est implémentée. Cette méthode est un moyen plus efficace de transférer des données. **TransferObjectDataOnClearChannel** est traité de la même façon que **TransferObjectData**, sauf que les données ne sont jamais chiffrées et n’ont pas de valeurs Mac à vérifier.

 

Les sections suivantes décrivent le processus de lecture et d’écriture, lorsque votre application implémente **IWMDMOperation**.

**Lire à partir d’un appareil**

lors de la lecture d’un fichier à partir d’un appareil, Windows Media Gestionnaire de périphériques appelle les méthodes **IWMDMOperation** suivantes dans l’ordre :

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Appelé pour avertir l’application qu’une lecture à partir d’un appareil commence.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Appelée une ou plusieurs fois. Le traitement des données est décrit dans les étapes suivantes :
    1.  **TransferObjectData** reçoit une mémoire tampon, *pData*, de taille *pdwSize* octets, remplie de données et un Mac pour vérifier les données entrantes.
    2.  L’application vérifie les paramètres entrants avec le MAC des données entrantes.
    3.  L’application déchiffre et lit autant de données que possible dans *pData* , et modifie la valeur retournée de *pdwSize* pour indiquer le nombre d’octets réellement lus.
    4.  L’application déchiffre les données, à l’aide de [**CSecureChannelClient ::D ecryptparam**](/previous-versions/bb231586(v=vs.85)), et les stocke ou les utilise, si nécessaire.
    5.  **TransferObjectData** retourne S \_ OK.
    6.  Windows media Gestionnaire de périphériques continue d’appeler **TransferObjectData** jusqu’à ce que l’application ait lu toutes les données du fichier, ou l’application renvoie WMDM \_ E \_ USER \_ cancelled pour annuler l’opération (auquel cas la lecture est annulée, et Windows Media Gestionnaire de périphériques appelle **End**).
-   [**Fin**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Appelé pour avertir l’application qu’une lecture à partir de l’appareil se termine.

**Écriture sur un appareil**

lors de l’écriture d’un fichier sur l’appareil, Windows Media Gestionnaire de périphériques appelle les méthodes **IWMDMOperation** suivantes dans l’ordre :

-   [**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Appelé pour permettre à l’application de spécifier un nom pour le nouveau stockage. Cette méthode est appelée uniquement si l’application n’a pas spécifié de nom dans la méthode **Insert** .
-   [**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Appelé pour permettre à l’application de spécifier des attributs pour le nouveau stockage sur l’appareil.
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Appelé pour avertir qu’une écriture sur l’appareil commence.
-   [**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) appelé pour extraire la taille totale de l’objet en cours d’écriture sur l’appareil, pour permettre l’optimisation du transfert, et pour donner à Windows média Gestionnaire de périphériques la possibilité d’annuler le transfert si le fichier est trop grand pour l’appareil.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Appelée une ou plusieurs fois. Le traitement des données est décrit dans les étapes suivantes :
    1.  **TransferObjectData** reçoit un pointeur vers une mémoire tampon de taille *pdwSize* octets.
    2.  L’application obtient un bloc de données à envoyer à l’appareil, généralement en lisant les données d’un fichier, et remplit la mémoire tampon de réception avec jusqu’à *pdwSize* d’octets. Il doit modifier *pdwSize* (si nécessaire) pour refléter le nombre d’octets ajoutés à la mémoire tampon.
    3.  L’application crée un MAC de tous les paramètres de la méthode.
    4.  L’application chiffre les données dans la mémoire tampon, à l’aide de [**CSecureChannelClient :: EncryptParam**](/previous-versions/bb231587(v=vs.85)).
    5.  **TransferObjectData** retourne s \_ OK pour indiquer qu’il y a plus de données, ou a la \_ valeur false pour indiquer qu’il n’y a plus de données. si l’application retourne l' \_ utilisateur WMDM E \_ \_ cancelled, l’opération d’écriture est annulée et Windows Media Gestionnaire de périphériques appellera **End**.
    6.  Windows Media Gestionnaire de périphériques continue d’appeler **TransferObjectData** tant que l’application renvoie la valeur \_ OK.
-   [**Fin**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Appelé pour avertir qu’une écriture sur l’appareil se termine.

Pour obtenir un exemple de code, consultez [chiffrement et déchiffrement](encryption-and-decryption.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’une Application de Gestionnaire de périphériques multimédia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 