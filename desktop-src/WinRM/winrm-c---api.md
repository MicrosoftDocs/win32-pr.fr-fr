---
title: API WinRM C++
description: les interfaces Windows Remote Management peuvent être utilisées pour obtenir des données ou gérer des ressources sur un ordinateur distant. Cette API est principalement destinée à un usage interne. Nous vous recommandons d’utiliser à la place l’API du shell client WinRM dans la mesure du possible.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742945"
---
# <a name="winrm-c-api"></a>API WinRM C++

les interfaces Windows Remote Management peuvent être utilisées pour obtenir des données ou gérer des [*ressources*](windows-remote-management-glossary.md) sur un ordinateur distant. Cette API est principalement destinée à un usage interne. Nous vous recommandons d’utiliser à la place l' [API du shell client WinRM](client-shell-api.md) dans la mesure du possible. Les interfaces correspondent étroitement à l' [API de script WinRM](winrm-scripting-api.md).

Les interfaces WinRM qui héritent directement de **IDispatch** ont chacune un objet de script correspondant. Pour plus d’informations, consultez l' [API de script WinRM](winrm-scripting-api.md).

Pour les applications multithread, WinRM ne prend pas en charge les threads distincts qui accèdent au même objet [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .

Les interfaces suivantes sont fournies par WinRM.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fournit des méthodes et des propriétés utilisées pour créer une nouvelle session et gérer une session établie. [**WSMan**](wsman.md) est l’objet de script correspondant.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fournit des méthodes et des propriétés utilisées pour créer un [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator). Cette méthode est disponible pour l’objet de script [**WSMan**](wsman.md) .

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Définit le nom d’utilisateur et le mot de passe utilisés pour les connexions à distance. [**ConnectionOptions**](connectionoptions.md) est l’objet de script correspondant.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Définit les opérations réseau et les propriétés disponibles pour la session. La [**session**](session.md) est l’objet de script correspondant.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Représente une collection de résultats retournés par l’énumération d’une ressource. L' [**énumérateur**](enumerator.md) est l’objet de script correspondant.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Fournit le chemin d’accès à une ressource. Vous pouvez utiliser un objet [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) à la place d’un [*URI de ressource*](windows-remote-management-glossary.md) dans les opérations d’objet de [**session**](session.md) . [**ResourceLocator**](resourcelocator.md) est l’objet de script correspondant.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Informations de référence sur la gestion à distance](windows-remote-management-reference.md)
</dt> </dl>

 

 




