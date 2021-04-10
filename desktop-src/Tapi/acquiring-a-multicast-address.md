---
description: Le fragment de code suivant montre comment demander et définir une adresse de multidiffusion pour une conférence.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Acquisition d’une adresse de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112614"
---
# <a name="acquiring-a-multicast-address"></a>Acquisition d’une adresse de multidiffusion

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le fragment de code suivant montre comment demander et définir une adresse de multidiffusion pour une conférence.

Par souci de simplicité, ce fragment montre l’affectation d’une adresse de multidiffusion à un élément multimédia. En réalité, la sélection d’une étendue, la demande d’adresse de multidiffusion et l’attribution sont effectuées pour chaque élément multimédia impliqué dans la Conférence.

Ce fragment part du principe que la [connexion à un serveur ils](connecting-to-an-ils-server.md) a déjà été effectuée. Les opérations présentées ici sont effectuées dans la section « modifier les paramètres si nécessaire » de la rubrique [création d’une annonce de conférence](creating-a-conference-announcement.md).


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces COM de multidiffusion](multicast-com-interfaces.md)
</dt> <dt>

[**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**IEnumBstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 



