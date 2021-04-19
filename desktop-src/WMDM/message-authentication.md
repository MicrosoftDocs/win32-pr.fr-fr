---
title: Authentification des messages
description: Authentification des messages
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Gestionnaire de périphériques Windows Media, authentification des messages
- Gestionnaire de périphériques, authentification des messages
- applications de bureau, authentification des messages
- fournisseurs de services, authentification des messages
- Guide de programmation, authentification des messages
- authentification des messages
- code d’authentification de message (MAC)
- MAC (code d’authentification de message)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511002"
---
# <a name="message-authentication"></a>Authentification des messages

L’authentification de message est un processus qui permet aux applications et aux fournisseurs de services de vérifier que les données transmises entre elles n’ont pas été falsifiées. Windows Media Gestionnaire de périphériques permet aux applications et aux fournisseurs de services d’effectuer l’authentification des messages à l’aide de codes d’authentification de message (MACs). Voici comment fonctionne l’authentification MAC :

L’expéditeur de données, généralement le fournisseur de services, passe un ou plusieurs éléments de données par le biais d’une fonction de chiffrement unidirectionnelle qui produit une signature unique, le MAC, pour toutes les données. L’expéditeur envoie ensuite tous les éléments signés de données avec le MAC au récepteur (généralement l’application). Le destinataire transmet les données via la même fonction de chiffrement pour générer un MAC et le compare au MAC qui a été envoyé. Si le MAC correspond, les données n’ont pas été modifiées.

Pour effectuer l’authentification MAC, l’application ou le fournisseur de services requiert une clé de chiffrement et un certificat correspondant. Pour plus d’informations sur l’emplacement à utiliser, consultez [outils de développement](tools-for-development.md).

Les étapes suivantes décrivent la manière dont les données sont signées par l’expéditeur et sont ensuite contrôlées par le destinataire. Dans Windows Media Gestionnaire de périphériques, le fournisseur de services utilise la classe [CSecureChannelServer](csecurechannelserver-class.md) pour générer des Mac, et l’application utilise la classe [CSecureChannelClient](csecurechannelclient-class.md) . Les deux classes fournissent des fonctions identiques avec des paramètres identiques, donc les étapes suivantes s’appliquent aux deux classes.

L’expéditeur (en général, le fournisseur de services) :

1.  Obtient les données à signer.
2.  Créez un nouveau handle MAC en appelant **MACInit**.
3.  Ajoutez un élément de données à signer dans le handle en appelant **MACUpdate**. Cette fonction accepte le handle créé précédemment, ainsi qu’une partie des données qui doivent être signées.
4.  Répétez l’étape 3 pour chaque élément de données supplémentaire qui doit être signé. Il n’a pas d’importance quant à l’ordre dans lequel les données sont ajoutées au MAC.
5.  Copiez le MAC du handle vers une nouvelle mémoire tampon d’octets en appelant **MACFinal**. Cette fonction accepte le handle MAC et une mémoire tampon que vous allouez, et copie le MAC à partir du handle dans la mémoire tampon fournie.

Lorsque vous effectuez une authentification MAC, il est important que l’expéditeur et le destinataire présentent les mêmes données dans le MAC. Pour les méthodes d’application qui fournissent un MAC, en général, tous les paramètres sont inclus dans la valeur MAC (à l’exception du MAC lui-même, bien entendu). Par exemple, considérez la méthode **IWMDMOperation :: TransferObjectData** :

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

Dans cette méthode, le MAC inclut *pData* et *pdwSize*. Si vous n’incluez pas les deux paramètres, le MAC que vous créez ne correspondra pas au MAC passé à *abMac*. Un fournisseur de services doit veiller à placer tous les paramètres requis dans la méthode d’application dans la valeur MAC.

Le code C++ suivant illustre la création d’un MAC dans l’implémentation d’un fournisseur de services de [**IMDSPStorageGlobals :: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



Le récepteur (en général, l’application) :

Si le destinataire n’a pas implémenté l’interface [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , il doit effectuer les mêmes étapes que l’expéditeur, puis comparer les deux valeurs Mac. L’exemple de code C++ suivant montre comment une application vérifie le MAC reçu dans un appel à [**IWMDMStorageGlobals :: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) pour s’assurer que le numéro de série n’a pas été falsifié en transit.


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de canaux authentifiés sécurisés**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




