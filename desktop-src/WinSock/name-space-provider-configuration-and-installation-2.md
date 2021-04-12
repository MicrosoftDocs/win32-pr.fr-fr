---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Configuration et installation du fournisseur d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c87de8fee4ccaea0fb6978037e1e41684b56267
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526140"
---
# <a name="namespace-provider-configuration-and-installation"></a>Configuration et installation du fournisseur d’espace de noms

-   [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**WSCWriteNameSpaceOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Comme mentionné précédemment, l’application d’installation d’un fournisseur d’espace de noms doit appeler [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) ou [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) pour s’inscrire auprès du \_32.dll Ws2 et fournir des informations de configuration statiques. Pour installer dans le catalogue 32 bits sur une plateforme 64 bits, le fournisseur d’espaces de noms doit appeler [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) ou [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32). Le \_32.dll Ws2 utilise ces informations pour accomplir sa fonction de routage et dans son implémentation de [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) et [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). La fonction [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) est utilisée pour supprimer un fournisseur d’espace de noms du Registre, et la fonction [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) est utilisée pour basculer un fournisseur entre les États actifs et inactifs.

Sur une plateforme 64 bits, [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) et [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) sont des fonctions similaires pour gérer le catalogue 32 bits.

Les résultats de ces trois opérations ne sont pas visibles pour les applications qui sont actuellement chargées et en cours d’exécution. Seules les applications qui commencent à s’exécuter après l’exécution de ces opérations seront affectées.

Cette architecture prend en charge explicitement l’instanciation de plusieurs fournisseurs d’espaces de noms au sein d’une même DLL. Toutefois, chaque fournisseur de ce type doit avoir un identificateur de fournisseur (GUID) d’espace de noms unique et un appel distinct à [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) ou [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) doit se produire pour chaque instanciation (sur les plateformes 64 bits, les fonctions du catalogue 32 bits sont [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) et [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)). Un tel fournisseur peut déterminer quelle instanciation est appelée, car l’identificateur du fournisseur d’espace de noms (NSP) apparaît en tant que paramètre dans chaque fonction NSP.

 

 



