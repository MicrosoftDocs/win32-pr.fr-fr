---
description: Moniteur réseau utilise la fonction d’exportation ParserAutoInstallInfo pour installer un analyseur. Quand ParserAutoInstallInfo est appelé, l’analyseur retourne une \_ structure PARSERDLLINFO PF contenant toutes les informations nécessaires à l’installation d’une dll de l’analyseur par Moniteur réseau.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implémentation de ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521143"
---
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="993bf-104">Implémentation de ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="993bf-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="993bf-105">Moniteur réseau utilise la fonction d’exportation [**ParserAutoInstallInfo**](parserautoinstallinfo.md) pour installer un analyseur.</span><span class="sxs-lookup"><span data-stu-id="993bf-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="993bf-106">Quand **ParserAutoInstallInfo** est appelé, l’analyseur retourne une [**structure \_ PARSERDLLINFO PF**](pf-parserdllinfo.md) contenant toutes les informations nécessaires à l’installation d’une dll de l’analyseur par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="993bf-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="993bf-107">Moniteur réseau conserve une liste d’analyseurs existants dans le fichier [*Parser.ini*](p.md) et crée un fichier ini distinct pour chaque analyseur installé.</span><span class="sxs-lookup"><span data-stu-id="993bf-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="993bf-108">Pendant le processus d’installation, la DLL de l’analyseur doit identifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="993bf-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="993bf-109">Nombre d’analyseurs dans la DLL, y compris un nom et une description de commentaire pour chaque analyseur.</span><span class="sxs-lookup"><span data-stu-id="993bf-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="993bf-110">Les protocoles qui précèdent le protocole de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="993bf-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="993bf-111">Les protocoles qui suivent le protocole de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="993bf-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="993bf-112">Moniteur réseau utilise les informations de protocole d’analyseur précédentes et suivantes pour mettre à jour les [*jeux de remise*](h.md) et les [*ensembles*](f.md) d’analyseurs que votre dll d’analyseur identifie.</span><span class="sxs-lookup"><span data-stu-id="993bf-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="993bf-113">La procédure suivante identifie les étapes nécessaires à l’implémentation de [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="993bf-114">**Pour implémenter ParserAutoInstallInfo**</span><span class="sxs-lookup"><span data-stu-id="993bf-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="993bf-115">Allouez une structure [**\_ PARSERDLLINFO PF**](pf-parserdllinfo.md) à l’aide de **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="993bf-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="993bf-116">Retournez la mémoire dans le tas à l’aide de **HeapFree**.</span><span class="sxs-lookup"><span data-stu-id="993bf-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="993bf-117">N’oubliez pas que cet appel doit également allouer une structure [**\_ PARSERINFO PF**](pf-parserinfo.md) pour chaque analyseur de la dll.</span><span class="sxs-lookup"><span data-stu-id="993bf-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="993bf-118">Spécifiez le nombre d’analyseurs (généralement un) que la DLL contient dans le membre **nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="993bf-119">Spécifiez un nom, un commentaire et un fichier d’aide facultatif dans les membres **szProtocolName**, **szComment** et **szHelpFile** de chaque structure [**\_ PARSERINFO de PF**](pf-parserinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="993bf-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="993bf-120">Spécifiez les protocoles qui précèdent chaque protocole DLL.</span><span class="sxs-lookup"><span data-stu-id="993bf-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="993bf-121">L’une des conditions suivantes s’applique à un jeu de remise entrant.</span><span class="sxs-lookup"><span data-stu-id="993bf-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="993bf-122">Si les protocoles précédents peuvent déterminer que votre protocole suit les données des protocoles précédents, définissez le membre **pWhoHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="993bf-123">Dans ce cas, votre protocole est ensuite ajouté aux [*jeux de remise*](h.md) des protocoles précédents.</span><span class="sxs-lookup"><span data-stu-id="993bf-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="993bf-124">Si les protocoles précédents ne peuvent pas déterminer que votre protocole suit les données des protocoles précédents, définissez **pWhoCanPrecedeMe** membre de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="993bf-125">Dans ce cas, le protocole est ensuite ajouté aux [*ensembles suivants*](f.md) des protocoles.</span><span class="sxs-lookup"><span data-stu-id="993bf-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="993bf-126">Spécifiez les protocoles qui suivent chaque protocole DLL.</span><span class="sxs-lookup"><span data-stu-id="993bf-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="993bf-127">L’une des conditions suivantes s’applique à un ensemble de suivi sortant.</span><span class="sxs-lookup"><span data-stu-id="993bf-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="993bf-128">Si votre protocole peut déterminer quels protocoles suivent en fonction des données de votre protocole, définissez le membre **pWhoDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="993bf-129">Dans ce cas, ces protocoles sont ajoutés au jeu de [*remise*](h.md) de vos protocoles.</span><span class="sxs-lookup"><span data-stu-id="993bf-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="993bf-130">Si votre protocole ne peut pas déterminer quels protocoles suivent en fonction des données de votre protocole, définissez le membre **pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="993bf-131">Dans ce cas, ces protocoles sont ajoutés à l' [*ensemble suivant*](f.md) de votre protocole.</span><span class="sxs-lookup"><span data-stu-id="993bf-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="993bf-132">Retournez la [**structure \_ PARSERDLLINFO PF**](pf-parserdllinfo.md) à Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="993bf-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="993bf-133">Voici une implémentation de base de [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="993bf-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="993bf-134">L’exemple de code est extrait de l’analyseur générique fourni par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="993bf-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



