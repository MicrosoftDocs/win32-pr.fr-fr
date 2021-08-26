---
description: Une fois que vous avez défini les niveaux de sécurité pour votre pointeur IWbemServices, vous pouvez accéder aux diverses fonctionnalités de WMI. Une fois que vous avez fini d’utiliser WMI, vous devez arrêter votre application.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Nettoyage et arrêt d’une application WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d2093b16491bcb600438d781fa833a09754fdc5d0cc8cc83feb710a6d2727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120909"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Nettoyage et arrêt d’une application WMI

Une fois que vous avez défini les niveaux de sécurité pour votre pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous pouvez accéder aux diverses fonctionnalités de WMI. Une fois que vous avez fini d’utiliser WMI, vous devez arrêter votre application.

La procédure suivante décrit comment nettoyer et arrêter une application WMI.

**Pour nettoyer et arrêter une application WMI**

1.  Libère toutes les interfaces COM ouvertes.

    Les deux interfaces principales dont vous devez vous souvenir sont [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) et [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

2.  Appeler [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

    Comme avec toutes les applications COM, vous devez appeler [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) à la fin de votre application.

3.  Quittez votre application.

    L’exemple de code suivant montre comment quitter une application cliente WMI.

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > La `pSvc` variable est de type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* , et la variable PLoc est de type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

Vous avez correctement initialisé COM, accédé à WMI et quitté votre application. Pour plus d’informations, consultez [exemple : création d’une application WMI](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
