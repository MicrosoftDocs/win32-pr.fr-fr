---
description: Cette rubrique fournit des exemples de code pertinents pour les principales étapes du développement d’une application de conversation avec l’API de regroupement pair, en fournissant un contexte pour chaque appel d’API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Création d’une application de conversation de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319193"
---
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="cbb89-103">Création d’une application de conversation de groupe</span><span class="sxs-lookup"><span data-stu-id="cbb89-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="cbb89-104">Cette rubrique fournit des exemples de code pertinents pour les principales étapes du développement d’une application de conversation avec l’API de regroupement pair, en fournissant un contexte pour chaque appel d’API.</span><span class="sxs-lookup"><span data-stu-id="cbb89-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="cbb89-105">Les comportements de l’interface utilisateur et la structure globale de l’application ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="cbb89-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="cbb89-106">L’exemple d’application complète de conversation de groupe homologue est fourni dans le kit de développement logiciel (SDK) homologue.</span><span class="sxs-lookup"><span data-stu-id="cbb89-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="cbb89-107">Cette rubrique fait référence aux fonctions fournies dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="cbb89-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="cbb89-108">Initialisation d’un groupe</span><span class="sxs-lookup"><span data-stu-id="cbb89-108">Initializing a Group</span></span>

<span data-ttu-id="cbb89-109">Lors de la construction d’une application de conversation, la première étape consiste à initialiser l’infrastructure de regroupement d’homologues en appelant [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) avec la version la plus récente prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbb89-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="cbb89-110">Dans ce cas, **la \_ \_ version du groupe homologue** est définie dans le fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="cbb89-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="cbb89-111">La version réellement prise en charge par l’infrastructure est retournée dans **peerVersion**.</span><span class="sxs-lookup"><span data-stu-id="cbb89-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="cbb89-112">Création d’un groupe</span><span class="sxs-lookup"><span data-stu-id="cbb89-112">Creating a Group</span></span>

<span data-ttu-id="cbb89-113">Une application de conversation doit être en mesure de créer un groupe homologue si aucun groupe n’est disponible pour la jointure, ou si l’utilisateur de l’application souhaite en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="cbb89-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="cbb89-114">Pour ce faire, vous devez créer une structure de [**\_ \_ Propriétés de groupe homologue**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) et la remplir avec les paramètres initiaux pour le groupe, y compris le classifieur pour le groupe homologue, le nom convivial, le nom d’homologue du créateur et la durée de vie de présence.</span><span class="sxs-lookup"><span data-stu-id="cbb89-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="cbb89-115">Une fois cette structure remplie, vous la transmettez à [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span><span class="sxs-lookup"><span data-stu-id="cbb89-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


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



## <a name="issuing-invitations"></a><span data-ttu-id="cbb89-116">Émission d’invitations</span><span class="sxs-lookup"><span data-stu-id="cbb89-116">Issuing Invitations</span></span>

<span data-ttu-id="cbb89-117">Lors de l’émission d’une invitation, les GMCs des invités doivent être obtenus.</span><span class="sxs-lookup"><span data-stu-id="cbb89-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="cbb89-118">Celles-ci peuvent être obtenues en appelant [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) sur l’invite avec leur nom d’identité.</span><span class="sxs-lookup"><span data-stu-id="cbb89-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="cbb89-119">En cas de réussite, les informations d’identité (le XML qui contient le certificat codé en base 64 avec la clé publique RSA) sont écrites dans un emplacement externe (un fichier, dans cet exemple) où l’invité peut l’obtenir et l’utiliser pour créer une invitation.</span><span class="sxs-lookup"><span data-stu-id="cbb89-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="cbb89-120">À ce stade, un mécanisme de livraison de l’invitation à l’invité doit être établi.</span><span class="sxs-lookup"><span data-stu-id="cbb89-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="cbb89-121">Il peut s’agir d’un courrier électronique ou d’une autre méthode sécurisée d’échange de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cbb89-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="cbb89-122">Dans l’exemple ci-dessous, l’invitation est écrite dans un fichier qui peut ensuite être transféré sur l’ordinateur de l’invité.</span><span class="sxs-lookup"><span data-stu-id="cbb89-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


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



<span data-ttu-id="cbb89-123">Les invitations, comme les identités, sont également émises en externe.</span><span class="sxs-lookup"><span data-stu-id="cbb89-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="cbb89-124">Dans cet exemple, l’invitation est écrite dans un fichier avec **fputws** , où l’invité peut l’obtenir et l’utiliser lors de l’appel de [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="cbb89-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="joining-a-peer-group"></a><span data-ttu-id="cbb89-125">Joindre un groupe homologue</span><span class="sxs-lookup"><span data-stu-id="cbb89-125">Joining a Peer Group</span></span>

<span data-ttu-id="cbb89-126">Si l’homologue tente de joindre un groupe homologue créé par un autre homologue, il a besoin d’une invitation de cet homologue.</span><span class="sxs-lookup"><span data-stu-id="cbb89-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="cbb89-127">Les invitations sont remises par un processus ou une application externe à l’invité et enregistrées dans un fichier local, spécifié dans l’exemple ci-dessous en tant que *pwzFileName*.</span><span class="sxs-lookup"><span data-stu-id="cbb89-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="cbb89-128">L’objet BLOB XML d’invitation est lu à partir du fichier dans **wzInvitation** et transmis à [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="cbb89-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="register-for-peer-events"></a><span data-ttu-id="cbb89-129">S’inscrire pour les événements homologues</span><span class="sxs-lookup"><span data-stu-id="cbb89-129">Register for Peer Events</span></span>

<span data-ttu-id="cbb89-130">Avant de vous connecter, vous devez vous inscrire pour chaque événement homologue pertinent pour l’application.</span><span class="sxs-lookup"><span data-stu-id="cbb89-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="cbb89-131">Dans l’exemple ci-dessous, vous vous inscrivez pour les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="cbb89-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="cbb89-132">enregistrement de l’événement du groupe HOMOLOGUe \_ \_ \_ \_ modifié.</span><span class="sxs-lookup"><span data-stu-id="cbb89-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="cbb89-133">Étant donné que les enregistrements seront utilisés pour contenir des messages de conversation publics, l’application doit être averti chaque fois qu’un nouvel est ajouté.</span><span class="sxs-lookup"><span data-stu-id="cbb89-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="cbb89-134">Lorsque cet événement homologue est reçu, les données d’événement exposent l’enregistrement avec le message de conversation.</span><span class="sxs-lookup"><span data-stu-id="cbb89-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="cbb89-135">Les applications doivent s’inscrire uniquement pour les types d’enregistrements qu’elles envisagent de gérer directement.</span><span class="sxs-lookup"><span data-stu-id="cbb89-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="cbb89-136">membre d’événement de groupe HOMOLOGUe \_ \_ \_ \_ modifié.</span><span class="sxs-lookup"><span data-stu-id="cbb89-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="cbb89-137">L’application doit être avertie lorsque des membres joignent ou laissent le groupe homologue afin que la liste des participants puisse être mise à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="cbb89-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="cbb89-138">État de l’événement du groupe HOMOLOGUe \_ \_ \_ \_ modifié.</span><span class="sxs-lookup"><span data-stu-id="cbb89-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="cbb89-139">Les modifications apportées à l’état du groupe homologue doivent être transmises à l’application.</span><span class="sxs-lookup"><span data-stu-id="cbb89-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="cbb89-140">Un membre du groupe homologue est considéré comme disponible dans le groupe homologue quand son état indique qu’il est connecté au groupe, synchronisé avec la base de données d’enregistrement du groupe homologue et qu’il écoute activement les mises à jour d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cbb89-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="cbb89-141">\_connexion directe d’événement de groupe homologue \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbb89-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="cbb89-142">Les messages privés entre deux membres et les échanges de données doivent être effectués via une connexion directe, de sorte que l’application doit être en mesure de gérer les demandes de connexion directe.</span><span class="sxs-lookup"><span data-stu-id="cbb89-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="cbb89-143">\_ \_ données entrantes de l’événement de groupe homologue \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbb89-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="cbb89-144">Après l’initialisation d’une connexion directe, cet événement homologue signale à l’application qu’un message privé a été reçu.</span><span class="sxs-lookup"><span data-stu-id="cbb89-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


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



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="cbb89-145">Connexion à un groupe homologue</span><span class="sxs-lookup"><span data-stu-id="cbb89-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="cbb89-146">Si vous avez créé ou rejoint le groupe et enregistré pour les événements appropriés, il est temps de passer en ligne et de démarrer une session de conversation active.</span><span class="sxs-lookup"><span data-stu-id="cbb89-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="cbb89-147">Pour ce faire, appelez [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) et transmettez le descripteur de groupe obtenu à partir de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) ou [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="cbb89-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="cbb89-148">Après l’appel de, les messages de conversation sont reçus en tant qu’événements de modification d’enregistrement d’événement de groupe d’HOMOLOGUe \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbb89-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="cbb89-149">Obtention d’une liste de membres du groupe homologue</span><span class="sxs-lookup"><span data-stu-id="cbb89-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="cbb89-150">L’obtention d’une liste de membres connectés au groupe pair est simple : appelez [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) pour récupérer la liste des membres du groupe, puis appelez [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) de manière itérative jusqu’à ce que tous les membres soient récupérés.</span><span class="sxs-lookup"><span data-stu-id="cbb89-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="cbb89-151">Vous devez appeler [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) après avoir traité chaque structure de membre, et vous devez fermer l’énumération en appelant [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="cbb89-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


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



## <a name="sending-a-chat-message"></a><span data-ttu-id="cbb89-152">Envoi d’un message de conversation</span><span class="sxs-lookup"><span data-stu-id="cbb89-152">Sending a Chat Message</span></span>

<span data-ttu-id="cbb89-153">Dans cet exemple, un message de conversation est envoyé en le plaçant dans le champ de **données** d’une structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="cbb89-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="cbb89-154">L’enregistrement est ajouté aux enregistrements du groupe homologue en appelant [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), qui le publiera et déclenchera l' \_ événement de \_ \_ modification de l’enregistrement d’événement de groupe pair \_ sur tous les pairs participant au groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="cbb89-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


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



## <a name="receiving-a-chat-message"></a><span data-ttu-id="cbb89-155">Réception d’un message de conversation</span><span class="sxs-lookup"><span data-stu-id="cbb89-155">Receiving a Chat Message</span></span>

<span data-ttu-id="cbb89-156">Pour recevoir le message de conversation, créez une fonction de rappel pour l' \_ événement de modification d’enregistrement d’événement de groupe pair \_ \_ \_ qui appelle une fonction semblable à celle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cbb89-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="cbb89-157">L’enregistrement est obtenu en appelant [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) sur les données d’événement reçues par un appel précédent à [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) dans la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="cbb89-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="cbb89-158">Le message de conversation est stocké dans le champ de **données** de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cbb89-158">The chat message is stored in the **data** field of this record.</span></span>


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



 

 



