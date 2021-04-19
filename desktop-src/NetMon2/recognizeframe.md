---
description: La fonction d’exportation RecognizeFrame indique si un élément de données est reconnu comme le protocole détecté par l’analyseur. La fonction d’exportation RecognizeFrame doit être implémentée pour chaque analyseur pris en charge par la DLL de l’analyseur.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Fonction de rappel RecognizeFrame (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535059"
---
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="e59ba-104">RecognizeFrame fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="e59ba-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="e59ba-105">La fonction d’exportation **RecognizeFrame** indique si un élément de données est reconnu comme le protocole détecté par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e59ba-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="e59ba-106">La fonction d’exportation **RecognizeFrame** doit être implémentée pour chaque analyseur pris en charge par la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e59ba-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59ba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e59ba-107">Syntax</span></span>


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="e59ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e59ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e59ba-109">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-110">Handle vers le frame qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="e59ba-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-111">*lpFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-112">Pointeur vers le premier octet d’un frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="e59ba-113">Le pointeur fournit un moyen d’afficher les données que les autres analyseurs reconnaissent.</span><span class="sxs-lookup"><span data-stu-id="e59ba-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-114">*lpProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-115">Pointeur vers le début des données inrécupérées.</span><span class="sxs-lookup"><span data-stu-id="e59ba-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="e59ba-116">En règle générale, les données non réclamées se trouvent au milieu d’une trame, car un analyseur précédent a demandé des données avant cet analyseur.</span><span class="sxs-lookup"><span data-stu-id="e59ba-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="e59ba-117">L’analyseur doit d’abord tester les données non réclamées.</span><span class="sxs-lookup"><span data-stu-id="e59ba-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-118">*MacType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-119">Valeur MAC du premier protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="e59ba-120">En règle générale, la valeur *MacType* est utilisée lorsque l’analyseur doit identifier le premier protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="e59ba-121">La valeur *MacType* peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="e59ba-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="e59ba-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e59ba-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="e59ba-123">Signification</span><span class="sxs-lookup"><span data-stu-id="e59ba-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="e59ba-124"><dt>**MAC \_ type \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="e59ba-125">802.3</span><span class="sxs-lookup"><span data-stu-id="e59ba-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="e59ba-126"><dt>**\_type Mac \_ TOKENRING**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="e59ba-127">802.5</span><span class="sxs-lookup"><span data-stu-id="e59ba-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="e59ba-128"><dt>**\_type Mac \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="e59ba-129">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="e59ba-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e59ba-130">*BytesLeft* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-131">Nombre d’octets restants à partir d’un emplacement dans un frame jusqu’à la fin du frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-132">*hPreviousProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-133">Handle du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="e59ba-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-134">*nPreviousProtocolOffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-135">Décalage du début du protocole précédent du frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-136">*ProtocolStatusCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-137">Indicateur d’état de protocole.</span><span class="sxs-lookup"><span data-stu-id="e59ba-137">Protocol status indicator.</span></span> <span data-ttu-id="e59ba-138">La DLL de l’analyseur doit définir l’un des codes d’état suivants.</span><span class="sxs-lookup"><span data-stu-id="e59ba-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="e59ba-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="e59ba-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="e59ba-140">Signification</span><span class="sxs-lookup"><span data-stu-id="e59ba-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="e59ba-141"><dt>**État du protocole \_ \_ reconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="e59ba-142">L’analyseur reconnaît les données, mais ne sait pas quel protocole suit.</span><span class="sxs-lookup"><span data-stu-id="e59ba-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="e59ba-143">Après avoir défini le code, retournez un pointeur vers les données non réclamées restantes qui suivent le protocole reconnu.</span><span class="sxs-lookup"><span data-stu-id="e59ba-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="e59ba-144">Moniteur réseau utilise le [*jeu suivant*](f.md) du protocole pour poursuivre l’analyse.</span><span class="sxs-lookup"><span data-stu-id="e59ba-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="e59ba-145"><dt>**État du protocole \_ \_ non \_ reconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="e59ba-146">L’analyseur ne reconnaît pas les données.</span><span class="sxs-lookup"><span data-stu-id="e59ba-146">The parser does not recognize the data.</span></span> <span data-ttu-id="e59ba-147">Après avoir défini ce code, retournez le pointeur au début des données à l’aide du pointeur que le paramètre *lpProtocol* transmet à la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e59ba-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="e59ba-148">Moniteur réseau utilise le *jeu suivant* du protocole précédent pour poursuivre l’analyse.</span><span class="sxs-lookup"><span data-stu-id="e59ba-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="e59ba-149"><dt>**État du protocole \_ \_ demandé**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="e59ba-150">L’analyseur reconnaît les données et prétend les données restantes.</span><span class="sxs-lookup"><span data-stu-id="e59ba-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="e59ba-151">Après avoir défini le code, retournez **null** pour moniteur réseau pour terminer l’analyse d’un frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="e59ba-152"><dt>**\_ \_ protocole suivant de l’état du protocole \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="e59ba-153">L’analyseur reconnaît les données et sait quel protocole suit.</span><span class="sxs-lookup"><span data-stu-id="e59ba-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="e59ba-154">Après avoir défini le code, définissez le paramètre *phNextProtocol* et retournez un pointeur vers les données non réclamées restantes qui suivent le protocole reconnu.</span><span class="sxs-lookup"><span data-stu-id="e59ba-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="e59ba-155">Moniteur réseau poursuit l’analyse du frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="e59ba-156">*phNextProtocol* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-157">Pointeur vers le handle du protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="e59ba-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="e59ba-158">Ce paramètre est défini lorsqu’un protocole identifie le protocole qui suit un protocole.</span><span class="sxs-lookup"><span data-stu-id="e59ba-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="e59ba-159">Pour obtenir le descripteur du protocole suivant, appelez la fonction [GetProtocolFromTable](getprotocolfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="e59ba-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e59ba-160">*lpInstData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e59ba-161">En entrée, pointeur vers les données d’instance du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="e59ba-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="e59ba-162">Lors de la sortie, pointeur vers les données d’instance pour le protocole en cours.</span><span class="sxs-lookup"><span data-stu-id="e59ba-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="e59ba-163">La longueur des données d’instance ne peut pas être supérieure à celle \_ d’un PTR DWORD.</span><span class="sxs-lookup"><span data-stu-id="e59ba-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e59ba-164">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e59ba-164">Return value</span></span>

<span data-ttu-id="e59ba-165">Si la fonction réussit, la valeur de retour est un pointeur vers le premier octet après les données de l’analyseur reconnues.</span><span class="sxs-lookup"><span data-stu-id="e59ba-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="e59ba-166">Si l’analyseur prétend toutes les données restantes, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="e59ba-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="e59ba-167">Si la fonction échoue, la valeur de retour est un pointeur initial que le paramètre *lpProtocol* passe.</span><span class="sxs-lookup"><span data-stu-id="e59ba-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="e59ba-168">Notes</span><span class="sxs-lookup"><span data-stu-id="e59ba-168">Remarks</span></span>

<span data-ttu-id="e59ba-169">La fonction **RecognizeFrame** détermine si l’analyseur reconnaît les données brutes en commençant au pointeur *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="e59ba-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="e59ba-170">Si le protocole reconnaît les données, la fonction **RecognizeFrame** retourne un pointeur vers les données restantes, ou retourne la **valeur null** si le protocole actuel est le dernier protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="e59ba-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="e59ba-171">Si le protocole ne reconnaît pas les données, la fonction **RecognizeFrame** retourne le pointeur passé à la dll de l’analyseur dans le paramètre *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="e59ba-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="e59ba-172">*RecognizeFrame* peut être appelé avant que la fonction [*Register*](register-parser.md) soit appelée pour enregistrer les propriétés de protocole.</span><span class="sxs-lookup"><span data-stu-id="e59ba-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="e59ba-173">Pour cette raison, l’implémentation de la fonction *RecognizeFrame* ne repose sur aucune propriété ou structure qui est créée ou initialisée pendant l’implémentation de la fonction de **registre** de protocole.</span><span class="sxs-lookup"><span data-stu-id="e59ba-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="e59ba-174">**Jeu de remise et ensemble de suivi**</span><span class="sxs-lookup"><span data-stu-id="e59ba-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="e59ba-175">Un analyseur peut utiliser un jeu de remise ou un ensemble de suivi pour identifier les Moniteur réseau le protocole qui suit les données reconnues.</span><span class="sxs-lookup"><span data-stu-id="e59ba-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="e59ba-176">Si des informations sont disponibles dans les données reconnues, l’analyseur utilise son jeu de remise pour obtenir un handle pour le protocole suivant, puis passe ce handle à Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e59ba-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="e59ba-177">Si aucune information n’est disponible, l’analyseur ne passe pas de handle et Moniteur réseau utilise le jeu de suivi de l’analyseur pour déterminer le protocole qui suit.</span><span class="sxs-lookup"><span data-stu-id="e59ba-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="e59ba-178">**Passage d’informations entre les protocoles**</span><span class="sxs-lookup"><span data-stu-id="e59ba-178">**Passing information between protocols**</span></span>

<span data-ttu-id="e59ba-179">Utilisez le paramètre *lpInstData* pour transmettre des informations entre les protocoles.</span><span class="sxs-lookup"><span data-stu-id="e59ba-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="e59ba-180">En entrée, vous pouvez récupérer les informations du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="e59ba-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="e59ba-181">Lors de la sortie, vous pouvez transmettre des informations au protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="e59ba-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="e59ba-182">Les données d’instance peuvent être des données qui sont inférieures ou égales à un \_ ptr DWORD en longueur, ou un pointeur vers des données, telles que des données de trame brutes, qui n’a pas besoin d’être alloué ou libéré par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e59ba-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="e59ba-183">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="e59ba-183">For Information on</span></span>                                        | <span data-ttu-id="e59ba-184">Consultez</span><span class="sxs-lookup"><span data-stu-id="e59ba-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e59ba-185">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e59ba-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="e59ba-186">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="e59ba-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="e59ba-187">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e59ba-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="e59ba-188">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="e59ba-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="e59ba-189">L’implémentation de **RecognizeFrame**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="e59ba-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="e59ba-190">Implémentation de RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="e59ba-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="e59ba-191">Comment spécifier un jeu de remise et un ensemble de suivi.</span><span class="sxs-lookup"><span data-stu-id="e59ba-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="e59ba-192">[Spécification d’un jeu de remise](specifying-a-handoff-set.md)[spécifiant un ensemble suivant](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="e59ba-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e59ba-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e59ba-193">Requirements</span></span>



| <span data-ttu-id="e59ba-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e59ba-194">Requirement</span></span> | <span data-ttu-id="e59ba-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="e59ba-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e59ba-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e59ba-196">Minimum supported client</span></span><br/> | <span data-ttu-id="e59ba-197">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e59ba-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e59ba-198">Minimum supported server</span></span><br/> | <span data-ttu-id="e59ba-199">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e59ba-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e59ba-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="e59ba-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="e59ba-201"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e59ba-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e59ba-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e59ba-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59ba-203">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="e59ba-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 




