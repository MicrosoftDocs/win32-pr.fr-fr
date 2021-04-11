---
title: Interface utilisateur de configuration de Server-Side
description: Implémentez une interface utilisateur de configuration pour le serveur en implémentant l’interface COM, IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0904c90fea2bef3ccc00c00135be09a711d8454
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314969"
---
# <a name="server-side-configuration-user-interface"></a>Interface utilisateur de configuration de Server-Side

Implémentez une interface utilisateur de configuration pour le serveur en implémentant l’interface COM, [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Cette interface COM est dérivée de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et ajoute trois méthodes : [**IEAPProviderConfig :: Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig :: ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)et [**IEAPProviderConfig :: Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

L’interface utilisateur doit prendre en charge l’administration à distance. En d’autres termes, bien que l’interface utilisateur configure le protocole d’authentification sur le serveur, l’interface utilisateur est peut-être en cours d’exécution sur un autre ordinateur. Pour prendre en charge l’administration à distance, séparez le code de l’interface utilisateur du code qui effectue réellement la configuration. Le code de configuration se trouve sur le serveur sur lequel s’exécute le protocole d’authentification.

Utilisez la Active Template Library (ATL) pour implémenter [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Pour plus d’informations, consultez l’exemple d’interface utilisateur de configuration côté serveur dans le répertoire des exemples du kit de développement logiciel (SDK). L’identificateur de classe (CLSID) de l’objet d’interface utilisateur de configuration doit être placé dans le Registre avec le nom de la valeur du CLSID de la [ \_ \_ \_ configuration \_ d’accès distant EAP](authentication-protocol-registry-values.md). Pour plus d’informations, consultez [valeurs de Registre du protocole d’authentification](authentication-protocol-registry-values.md).

Quand l’utilisateur clique sur le bouton configurer pour un protocole d’authentification dans la boîte de dialogue Propriétés pour le routage et le service d’accès à distance, le système vérifie si une valeur CLSID de la configuration du service d’accès distant \_ EAP \_ \_ \_ pour ce protocole d’authentification existe dans le registre. Si c’est le cas, COM instancie l’objet d’interface utilisateur de configuration. Si le système ne parvient pas à trouver le \_ \_ CLSID de la configuration du service d’accès distant EAP \_ \_ dans le registre et que le système a accès aux services d’annuaire (DS), le système tente d’instancier l’objet à partir du magasin de classes.

Dans le cas où l’utilisateur est connecté simultanément à plusieurs ordinateurs, plusieurs objets d’interface utilisateur de configuration sont instanciés.

 

 