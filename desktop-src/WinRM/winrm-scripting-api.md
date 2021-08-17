---
title: API de script WinRM
description: Windows Les objets de script de gestion à distance sont implémentés en tant que couche au-dessus du protocole WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742757"
---
# <a name="winrm-scripting-api"></a>API de script WinRM

Windows Les objets de script de gestion à distance sont implémentés en tant que couche au-dessus du [protocole WS-Management](ws-management-protocol.md). Les objets de script vous permettent d’obtenir des données ou de gérer des [*ressources*](windows-remote-management-glossary.md) sur des ordinateurs locaux et distants.

## <a name="ws-management-objects"></a>Objets WS-Management

Chaque objet de script a une interface C++ correspondante. pour plus d’informations, consultez [API C++ WinRM](winrm-c---api.md) et [scripts dans Windows Remote Management](scripting-in-windows-remote-management.md).

Les objets suivants sont fournis par l’API de script WinRM.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Définit le nom d’utilisateur et le mot de passe utilisés pour les connexions à distance. Le nom d’utilisateur et le mot de passe sont transmis lors de l’appel de la méthode [**CreateConnectionOptions**](wsman-createconnectionoptions.md) . Pour plus d’informations, consultez [obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md). L’interface C++ correspondante est [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Énumérateur**](enumerator.md)
</dt> <dd>

Représente une collection de résultats retournés par l’énumération d’une ressource. Pour plus d’informations, consultez [énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md). L’interface C++ correspondante est [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Fournit le chemin d’accès à une ressource. Vous pouvez utiliser un objet [**ResourceLocator**](resourcelocator.md) à la place d’un [*URI de ressource*](windows-remote-management-glossary.md) dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md). L’interface C++ correspondante est [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)
</dt> <dd>

Définit les opérations réseau et les propriétés disponibles pour la session, telles que [**session. obtenir**](session-get.md), [**session. Enumerate**](session-enumerate.md), [**session. Invoke**](session-invoke.md). Pour plus d’informations, consultez [obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md). L’interface C++ correspondante est [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

Fournit des méthodes et des propriétés utilisées pour créer une session ou gérer une session établie. pour plus d’informations, consultez [utilisation de Windows Remote Management](using-windows-remote-management.md). Les interfaces C++ correspondantes sont [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) et [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows Informations de référence sur la gestion à distance](windows-remote-management-reference.md)
</dt> </dl>

 

 




