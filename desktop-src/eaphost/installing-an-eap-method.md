---
title: Installation d’une méthode EAP
description: Suivez les instructions ci-dessous pour installer une méthode EAP implémentée par l’utilisateur sur un ordinateur client exécutant EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021579"
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

 

 