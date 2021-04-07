---
title: Installation d’une méthode EAP
description: Suivez les instructions ci-dessous pour installer une méthode EAP implémentée par l’utilisateur sur un ordinateur client exécutant EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726285"
---
# <a name="installing-an-eap-method"></a>Installation d’une méthode EAP

Suivez les instructions ci-dessous pour installer une méthode EAP implémentée par l’utilisateur sur un ordinateur client exécutant EAPHost.

-   Implémentez [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DLLUNREGISTERSERVER**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) pour votre dll de méthode EAP. Ces fonctions ajoutent et suppriment les clés de Registre appropriées pour votre méthode EAP pendant le processus d’installation et de (désinstallation).

    Pour plus d’informations sur les clés de Registre spécifiques associées à l’installation d’une méthode EAP, consultez la rubrique [configuration du Registre pour les méthodes EAP](registry-keys-for-eap-methods.md) .

-   Installez la DLL qui contient l’implémentation de la méthode EAP à l’aide de la commande de console suivante.

     *&lt; Nom &gt;* de la dllregsvr32.exe

    Pour désinstaller la DLL, utilisez la commande de console suivante :

    **regsvr32.exe** **/u** *&lt; nom &gt;* de la dll

-   Redémarrez le service EAPHost.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> </dl>

 

 