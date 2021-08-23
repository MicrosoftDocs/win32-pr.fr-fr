---
description: Cette rubrique fournit des exemples de code pertinents pour les principales étapes du développement d’une application de conversation avec l’API de regroupement pair, en fournissant un contexte pour chaque appel d’API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Création d’une application de conversation de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb8f9458f8e01bea86e42f0cd976395e951bda52f13af46952479d5810e46c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011657"
---
# <a name="creating-a-group-chat-application"></a>Création d’une application de conversation de groupe

Cette rubrique fournit des exemples de code pertinents pour les principales étapes du développement d’une application de conversation avec l’API de regroupement pair, en fournissant un contexte pour chaque appel d’API. Les comportements de l’interface utilisateur et la structure globale de l’application ne sont pas inclus.

> [!Note]  
> L’exemple d’application complète de conversation de groupe homologue est fourni dans le kit de développement logiciel (SDK) homologue. Cette rubrique fait référence aux fonctions fournies dans l’exemple.

 

## <a name="initializing-a-group"></a>Initialisation d’un groupe

Lors de la construction d’une application de conversation, la première étape consiste à initialiser l’infrastructure de regroupement d’homologues en appelant [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) avec la version la plus récente prise en charge. Dans ce cas, **la \_ \_ version du groupe homologue** est définie dans le fichier d’en-tête de l’application. La version réellement prise en charge par l’infrastructure est retournée dans **peerVersion**.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Création d’un groupe

Une application de conversation doit être en mesure de créer un groupe homologue si aucun groupe n’est disponible pour la jointure, ou si l’utilisateur de l’application souhaite en créer un nouveau. Pour ce faire, vous devez créer une structure de [**\_ \_ Propriétés de groupe homologue**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) et la remplir avec les paramètres initiaux pour le groupe, y compris le classifieur pour le groupe homologue, le nom convivial, le nom d’homologue du créateur et la durée de vie de présence. Une fois cette structure remplie, vous la transmettez à [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a>Émission d’invitations

Lors de l’émission d’une invitation, les GMCs des invités doivent être obtenus. Celles-ci peuvent être obtenues en appelant [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) sur l’invite avec leur nom d’identité. En cas de réussite, les informations d’identité (le XML qui contient le certificat codé en base 64 avec la clé publique RSA) sont écrites dans un emplacement externe (un fichier, dans cet exemple) où l’invité peut l’obtenir et l’utiliser pour créer une invitation.

À ce stade, un mécanisme de livraison de l’invitation à l’invité doit être établi. Il peut s’agir d’un courrier électronique ou d’une autre méthode sécurisée d’échange de fichiers. Dans l’exemple ci-dessous, l’invitation est écrite dans un fichier qui peut ensuite être transféré sur l’ordinateur de l’invité.


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



Les invitations, comme les identités, sont également émises en externe. Dans cet exemple, l’invitation est écrite dans un fichier avec **fputws** , où l’invité peut l’obtenir et l’utiliser lors de l’appel de [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a>Joindre un groupe homologue

Si l’homologue tente de joindre un groupe homologue créé par un autre homologue, il a besoin d’une invitation de cet homologue. Les invitations sont remises par un processus ou une application externe à l’invité et enregistrées dans un fichier local, spécifié dans l’exemple ci-dessous en tant que *pwzFileName*. L’objet BLOB XML d’invitation est lu à partir du fichier dans **wzInvitation** et transmis à [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a>S’inscrire pour les événements homologues

Avant de vous connecter, vous devez vous inscrire pour chaque événement homologue pertinent pour l’application. Dans l’exemple ci-dessous, vous vous inscrivez pour les événements suivants :

-   enregistrement de l’événement du groupe HOMOLOGUe \_ \_ \_ \_ modifié. Étant donné que les enregistrements seront utilisés pour contenir des messages de conversation publics, l’application doit être averti chaque fois qu’un nouvel est ajouté. Lorsque cet événement homologue est reçu, les données d’événement exposent l’enregistrement avec le message de conversation. Les applications doivent s’inscrire uniquement pour les types d’enregistrements qu’elles envisagent de gérer directement.
-   membre d’événement de groupe HOMOLOGUe \_ \_ \_ \_ modifié. L’application doit être avertie lorsque des membres joignent ou laissent le groupe homologue afin que la liste des participants puisse être mise à jour en conséquence.
-   État de l’événement du groupe HOMOLOGUe \_ \_ \_ \_ modifié. Les modifications apportées à l’état du groupe homologue doivent être transmises à l’application. Un membre du groupe homologue est considéré comme disponible dans le groupe homologue quand son état indique qu’il est connecté au groupe, synchronisé avec la base de données d’enregistrement du groupe homologue et qu’il écoute activement les mises à jour d’enregistrement.
-   \_connexion directe d’événement de groupe homologue \_ \_ \_ . Les messages privés entre deux membres et les échanges de données doivent être effectués via une connexion directe, de sorte que l’application doit être en mesure de gérer les demandes de connexion directe.
-   \_ \_ données entrantes de l’événement de groupe homologue \_ \_ . Après l’initialisation d’une connexion directe, cet événement homologue signale à l’application qu’un message privé a été reçu.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a>Connexion à un groupe homologue

Si vous avez créé ou rejoint le groupe et enregistré pour les événements appropriés, il est temps de passer en ligne et de démarrer une session de conversation active. Pour ce faire, appelez [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) et transmettez le descripteur de groupe obtenu à partir de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) ou [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Après l’appel de, les messages de conversation sont reçus en tant qu’événements de modification d’enregistrement d’événement de groupe d’HOMOLOGUe \_ \_ \_ \_ .

## <a name="obtaining-a-list-of-peer-group-members"></a>Obtention d’une liste de membres du groupe homologue

L’obtention d’une liste de membres connectés au groupe pair est simple : appelez [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) pour récupérer la liste des membres du groupe, puis appelez [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) de manière itérative jusqu’à ce que tous les membres soient récupérés. Vous devez appeler [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) après avoir traité chaque structure de membre, et vous devez fermer l’énumération en appelant [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) lorsque le traitement est terminé.


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a>Envoi d’un message de conversation

Dans cet exemple, un message de conversation est envoyé en le plaçant dans le champ de **données** d’une structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) . L’enregistrement est ajouté aux enregistrements du groupe homologue en appelant [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), qui le publiera et déclenchera l' \_ événement de \_ \_ modification de l’enregistrement d’événement de groupe pair \_ sur tous les pairs participant au groupe homologue.


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a>Réception d’un message de conversation

Pour recevoir le message de conversation, créez une fonction de rappel pour l' \_ événement de modification d’enregistrement d’événement de groupe pair \_ \_ \_ qui appelle une fonction semblable à celle ci-dessous. L’enregistrement est obtenu en appelant [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) sur les données d’événement reçues par un appel précédent à [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) dans la fonction de rappel. Le message de conversation est stocké dans le champ de **données** de cet enregistrement.


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



