---
description: Moniteur réseau utilise la fonction d’exportation ParserAutoInstallInfo pour installer un analyseur. Quand ParserAutoInstallInfo est appelé, l’analyseur retourne une \_ structure PARSERDLLINFO PF contenant toutes les informations nécessaires à l’installation d’une dll de l’analyseur par Moniteur réseau.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implémentation de ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743079"
---
# <a name="implementing-parserautoinstallinfo"></a>Implémentation de ParserAutoInstallInfo

Moniteur réseau utilise la fonction d’exportation [**ParserAutoInstallInfo**](parserautoinstallinfo.md) pour installer un analyseur. Quand **ParserAutoInstallInfo** est appelé, l’analyseur retourne une [**structure \_ PARSERDLLINFO PF**](pf-parserdllinfo.md) contenant toutes les informations nécessaires à l’installation d’une dll de l’analyseur par Moniteur réseau.

> [!Note]  
> Moniteur réseau conserve une liste d’analyseurs existants dans le fichier [*Parser.ini*](p.md) et crée un fichier ini distinct pour chaque analyseur installé.

 

Pendant le processus d’installation, la DLL de l’analyseur doit identifier les éléments suivants :

-   Nombre d’analyseurs dans la DLL, y compris un nom et une description de commentaire pour chaque analyseur.
-   Les protocoles qui précèdent le protocole de l’analyseur.
-   Les protocoles qui suivent le protocole de l’analyseur.

> [!Note]  
> Moniteur réseau utilise les informations de protocole d’analyseur précédentes et suivantes pour mettre à jour les [*jeux de remise*](h.md) et les [*ensembles*](f.md) d’analyseurs que votre dll d’analyseur identifie.

 

La procédure suivante identifie les étapes nécessaires à l’implémentation de [**ParserAutoInstallInfo**](parserautoinstallinfo.md).

**Pour implémenter ParserAutoInstallInfo**

1.  Allouez une structure [**\_ PARSERDLLINFO PF**](pf-parserdllinfo.md) à l’aide de **HeapAlloc**.
2.  Retournez la mémoire dans le tas à l’aide de **HeapFree**.
3.  N’oubliez pas que cet appel doit également allouer une structure [**\_ PARSERINFO PF**](pf-parserinfo.md) pour chaque analyseur de la dll.
4.  Spécifiez le nombre d’analyseurs (généralement un) que la DLL contient dans le membre **nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).
5.  Spécifiez un nom, un commentaire et un fichier d’aide facultatif dans les membres **szProtocolName**, **szComment** et **szHelpFile** de chaque structure [**\_ PARSERINFO de PF**](pf-parserinfo.md) .
6.  Spécifiez les protocoles qui précèdent chaque protocole DLL. L’une des conditions suivantes s’applique à un jeu de remise entrant.
    -   Si les protocoles précédents peuvent déterminer que votre protocole suit les données des protocoles précédents, définissez le membre **pWhoHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Dans ce cas, votre protocole est ensuite ajouté aux [*jeux de remise*](h.md) des protocoles précédents.
    -   Si les protocoles précédents ne peuvent pas déterminer que votre protocole suit les données des protocoles précédents, définissez **pWhoCanPrecedeMe** membre de [**PF \_ PARSERINFO**](pf-parserinfo.md). Dans ce cas, le protocole est ensuite ajouté aux [*ensembles suivants*](f.md) des protocoles.
7.  Spécifiez les protocoles qui suivent chaque protocole DLL. L’une des conditions suivantes s’applique à un ensemble de suivi sortant.
    -   Si votre protocole peut déterminer quels protocoles suivent en fonction des données de votre protocole, définissez le membre **pWhoDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Dans ce cas, ces protocoles sont ajoutés au jeu de [*remise*](h.md) de vos protocoles.
    -   Si votre protocole ne peut pas déterminer quels protocoles suivent en fonction des données de votre protocole, définissez le membre **pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Dans ce cas, ces protocoles sont ajoutés à l' [*ensemble suivant*](f.md) de votre protocole.
8.  Retournez la [**structure \_ PARSERDLLINFO PF**](pf-parserdllinfo.md) à Moniteur réseau.

Voici une implémentation de base de [**ParserAutoInstallInfo**](parserautoinstallinfo.md). L’exemple de code est extrait de l’analyseur générique fourni par Moniteur réseau.

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

 

 



