---
description: L’API de distribution d’homologue définit les types de données suivants.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Types de données de l’API de distribution d’homologue (Peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ecfb7a9a90cb5ef2d79a20356ea8ea39f708874e85c3119dd4407a0a3758146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776079"
---
# <a name="peer-distribution-api-data-types"></a>Types de données de l’API de distribution d’homologue

L’API de distribution d’homologue définit les types de données suivants.


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| Type de données                                                                                                                     | Description                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_handle d’instance PEERDIST \_**          | Handle associé à l’instance de distribution d’homologue. Ce handle est créé par [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)et utilisé dans la plupart des opérations de distribution d’homologue.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_descripteur de contenu PEERDIST \_**             | Handle associé au contenu. Ce handle est créé par [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) et est référencé lors de l’ouverture, de la fermeture, de l’ajout ou de la publication de contenu.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_descripteur PEERDIST CONTENTINFO \_** | Handle associé aux informations de contenu. Ce handle est créé par [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)et est utilisé lors de la récupération des informations de contenu encodé.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_handle de flux PEERDIST \_**                | Handle associé à un flux de données. Ce handle est créé par [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) et est référencé lors de la publication, de la fermeture ou de l’ajout du contenu diffusé en continu.<br/>        |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Professionnel \[ applications de bureau uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Peerdist. h</dt> </dl> |



 

 




