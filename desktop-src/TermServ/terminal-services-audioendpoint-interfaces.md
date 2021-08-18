---
title: Services Bureau à distance les interfaces AudioEndpoint
description: Les interfaces suivantes sont utilisées avec l’API AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec12cd3d4648f3ed357e898f75850e77b3b679d59a92d9f0518f809ba52f58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000069"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Services Bureau à distance les interfaces AudioEndpoint

Les interfaces suivantes sont utilisées avec l’API AudioEndpoint.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Initialise un objet de point de terminaison d’appareil et obtient les fonctionnalités de l’appareil qu’il représente.

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Fournit des informations au moteur audio sur un point de terminaison audio. Cette interface est implémentée par un point de terminaison audio.

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Contrôle l’état du flux d’un point de terminaison.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Obtient la différence entre les positions actuelles de lecture et d’écriture dans la mémoire tampon du point de terminaison.

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Obtient la mémoire tampon d’entrée pour chaque passe de traitement.

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Obtient la mémoire tampon de sortie pour chaque passe de traitement.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’API Services Bureau à distance AudioEndpoint est destinée à être utilisée dans Bureau à distance scénarios ; ce n’est pas le cas pour les applications clientes.

 

 




