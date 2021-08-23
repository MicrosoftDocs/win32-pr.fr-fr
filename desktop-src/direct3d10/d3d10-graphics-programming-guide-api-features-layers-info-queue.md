---
description: Personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212b78352ccc9139c069ca5d388993fd83aca6833d77547a91401bc40380fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753829"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)

La file d’attente d’informations est gérée par une interface (voir [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) qui stocke, récupère et filtre les messages de débogage. La file d’attente comprend : une file d’attente de messages, une pile de filtres de stockage facultative et une pile de filtres de récupération facultative. La pile de filtre de stockage peut être utilisée pour filtrer les messages que vous souhaitez stocker. la pile de filtres de récupération peut être utilisée pour filtrer les messages que vous souhaitez stocker. Une fois que vous avez filtré un message, le message est affiché dans la fenêtre de débogage et stocké dans la pile appropriée.

En général :

-   Appeler [**ID3D10InfoQueue :: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) pour générer des messages définis par l’utilisateur
-   L’appel de [**ID3D10InfoQueue :: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) est utilisé pour recevoir des messages (qui passent un filtre de récupération facultatif).

## <a name="registry-controls"></a>Contrôles du Registre

Utilisez les clés de Registre pour ajuster les paramètres de filtre, ajuster les points d’arrêt et désactiver la sortie de débogage. La couche de débogage vérifie ces chemins d’accès pour les clés de Registre ; le premier chemin d’accès trouvé sera utilisé.

1.  \\Logiciel HKCU logiciel \\ Microsoft \\ Direct3D \\<sous-clé définie par l’utilisateur>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D \\<sous-clé définie par l’utilisateur>
3.  \\Logiciel HKCU \\ Microsoft \\ Direct3D

Où :

-   Socle HKCU pour HKEY \_ Current \_ User et HKLM stand pour HKEY \_ local \_ machine.
-   <> de sous-clé définie par l’utilisateur est un nom arbitraire pour stocker les paramètres de débogage d’une application

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtrage des messages de débogage à l’aide de clés de Registre

Si le registre contient une clé InfoQueueStorageFilterOverride (et est différent de zéro), les messages (et la sortie de débogage) peuvent être filtrés en ajoutant les contrôles de registre suivants.

-   DWORD muet \_ catégorie \_ \* -sortie de débogage si cette clé est différente de zéro.
-   \_Gravité de silence DWORD \_ \* -la sortie de débogage est désactivée si cette clé n’est pas nulle.
-   \_ID de sourdine DWORD \_ \* : le nom ou le numéro du message peut être utilisé pour \* (comme pour l' \_ ID BreakOn \_ \* décrit précédemment). La sortie de débogage est désactivée si cette clé est différente de zéro.
-   \_Info de gravité d' \_ inactivation DWORD-la sortie de débogage est activée si cette clé n’est pas nulle. Par défaut, quand InfoQueueStorageFilterOverride est activé, les messages de débogage avec des informations de gravité sont muets. par conséquent, pour cette clé, les informations sont retournées.

Ces contrôles modifient si un message est enregistré ou affiché ; ils n’affectent pas si une API réussit ou échoue.

### <a name="setting-break-conditions-using-registry-keys"></a>Définition de conditions d’arrêt à l’aide de clés de Registre

Les applications peuvent être forcées à s’arrêter sur un message à l’aide des clés de Registre suivantes.

**EnableBreakOnMessage** : cette clé permet de rompre les messages (et entraîne l’ignorance des paramètres de SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID ()). Les messages réels sur lesquels s’arrêter sont définis à l’aide d’une ou de plusieurs \_ \* valeurs BreakOn définies ci-dessous.

-   **BreakOn \_ \_Catégorie \** _ Break sur un message passant par les filtres de stockage. \_ est l’un des \_ messages de catégorie de message D3D10 \_ .
-   **BreakOn \_ \_Gravité \**: arrêt sur un message passant par les filtres de stockage. \_ est l’un des \_ messages de gravité du message D3D10 \_ \_ .
-   **BreakOn \_ \_ID \** _ Break sur un message passant par les filtres de stockage. \_ est l’un des \_ messages d' \_ ID de message D3D10 \_ ou peut être la valeur numérique de l’énumération d’erreur. Par exemple, supposons que le message avec l’ID « D3D10 \_ message \_ ID \_ hypothétique » contenait la valeur 123 dans l' \_ énumération de l’ID de message D3D10 \_ . Dans ce cas, la création de la valeur BreakOn \_ ID \_ hypothétique = 1 ou BreakOn \_ ID \_ 123 = 1 permet d’effectuer la même opération-Break lorsqu’un message ayant l’ID de message D3D10 ID \_ \_ \_ hypothétique est rencontré.

### <a name="muting-debug-output-using-registry-keys"></a>Désactiver la sortie de débogage à l’aide de clés de Registre

La sortie de débogage peut être muette à l’aide d’une clé MuteDebugOutput. La présence de cette valeur dans le registre force la substitution de la méthode [**ID3D10InfoQueue :: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) de InfoQueue. MuteDebugOutput arrête les messages qui passent le filtre de stockage à être envoyés à la sortie de débogage.

## <a name="disabling-debug-layer-messages"></a>Désactivation des messages de la couche de débogage

Les messages de couche de débogage peuvent être isolés ou en tant que groupe lors de l’exécution en spécifiant des filtres à l’aide de [**ID3D10InfoQueue :: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). L’argument *pFilter* de **ID3D10InfoQueue :: AddStorageFilterEntries** prend une structure de [**\_ \_ \_ filtre de file d’attente d’informations D3D10**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) qui contient une liste verte et une liste d’exclusion. Les listes d’autorisation et de refus sont décrites par les structures DESC de filtre de la [**\_ \_ file d’attente \_ \_ D3D10s**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) qui permettent de spécifier le filtrage par catégorie, gravité et ID de message individuel.

Le code suivant est un exemple de configuration de l' [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) pour refuser l’ID de message D3D10 de la \_ \_ mémoire tampon d’index de dessin de l’appareil un \_ \_ \_ \_ \_ \_ message trop petit.


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Couches d’API](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[Fonctionnalités de l’API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



