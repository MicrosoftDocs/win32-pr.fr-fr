---
description: Manipule une description de conférence textuelle.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interface ITConferenceBlob (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527308"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="edb6b-103">Interface ITConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="edb6b-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="edb6b-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="edb6b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="edb6b-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="edb6b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="edb6b-106">L’interface **ITConferenceBlob** manipule une description de conférence textuelle.</span><span class="sxs-lookup"><span data-stu-id="edb6b-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="edb6b-107">L’interface est destinée à être indépendante du format et de la syntaxe de la description de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="edb6b-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="edb6b-108">Pour manipuler des aspects spécifiques de la description de la Conférence, l’application doit interroger une autre interface.</span><span class="sxs-lookup"><span data-stu-id="edb6b-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="edb6b-109">Actuellement, seules les descriptions de conférence SDP sont prises en charge ; l’application doit utiliser **QueryInterface** pour [**ITSdp**](itsdp.md) pour accéder aux différents champs de la description de la Conférence SDP.</span><span class="sxs-lookup"><span data-stu-id="edb6b-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="edb6b-110">L’interface **ITConferenceBlob** est créée en appelant **QueryInterface** sur [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="edb6b-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="edb6b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="edb6b-111">Members</span></span>

<span data-ttu-id="edb6b-112">L’interface **ITConferenceBlob** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="edb6b-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="edb6b-113">**ITConferenceBlob** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="edb6b-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="edb6b-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="edb6b-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="edb6b-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="edb6b-115">Methods</span></span>

<span data-ttu-id="edb6b-116">L’interface **ITConferenceBlob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="edb6b-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="edb6b-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="edb6b-117">Method</span></span>                                                             | <span data-ttu-id="edb6b-118">Description</span><span class="sxs-lookup"><span data-stu-id="edb6b-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edb6b-119">**Obtient \_ CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="edb6b-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="edb6b-120">Obtient l’indicateur de [**\_ \_ jeu de caractères BLOB**](blob-character-set.md) indiquant si les caractères BLOB sont au format ASCII, Unicode, etc.</span><span class="sxs-lookup"><span data-stu-id="edb6b-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="edb6b-121">**Obtient \_ ConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="edb6b-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="edb6b-122">Obtient un pointeur vers l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="edb6b-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="edb6b-123">**Rein**</span><span class="sxs-lookup"><span data-stu-id="edb6b-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="edb6b-124">Initialise l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="edb6b-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="edb6b-125">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="edb6b-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="edb6b-126">Valide les modifications apportées à l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="edb6b-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="edb6b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edb6b-127">Requirements</span></span>



| <span data-ttu-id="edb6b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edb6b-128">Requirement</span></span> | <span data-ttu-id="edb6b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="edb6b-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edb6b-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="edb6b-130">TAPI version</span></span><br/> | <span data-ttu-id="edb6b-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="edb6b-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="edb6b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="edb6b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="edb6b-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb6b-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="edb6b-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="edb6b-134">Library</span></span><br/>      | <dl> <span data-ttu-id="edb6b-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edb6b-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="edb6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="edb6b-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="edb6b-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edb6b-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

