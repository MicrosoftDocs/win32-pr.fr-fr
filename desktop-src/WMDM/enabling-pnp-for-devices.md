---
title: Activation de PnP pour les appareils
description: Activation de PnP pour les appareils
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Gestionnaire de périphériques de média, appareils PnP
- Gestionnaire de périphériques, appareils PnP
- Guide de programmation, appareils PnP
- fournisseurs de services, appareils PnP
- création de fournisseurs de services, de périphériques PnP
- Périphériques PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856450"
---
# <a name="enabling-pnp-for-devices"></a>Activation de PnP pour les appareils

Windows Media Gestionnaire de périphériques surveille les notifications d’arrivée et de suppression des appareils qui publient une interface de périphérique de lecteur audio portable. à l’arrivée d’un tel appareil, Windows Media Gestionnaire de périphériques interroge un paramètre d’appareil nommé *WMDMSPCLSID* pour l’ID de classe du fournisseur de services responsable de cet appareil. Windows Le Gestionnaire de périphériques multimédia appelle [**IMDServiceProvider2 :: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) sur ce fournisseur de services pour créer un objet appareil, qui est exposé à l’application sous la forme d’un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

Un fournisseur de services peut soit gérer des appareils PnP, soit des appareils non Plug-and-Play ; il ne peut pas gérer les deux types.

pour qu’un appareil fonctionne avec le mécanisme précédent (et qui, par conséquent, active les notifications d’arrivée et de suppression pour l’appareil sous Windows applications Gestionnaire de périphériques multimédia), les conditions suivantes doivent être remplies :

-   le pilote de périphérique de cet appareil doit publier le média Windows Gestionnaire de périphériques interface du périphérique Portable Audio Player. Le GUID de cette interface d’appareil est défini comme suit :

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Un appareil ne doit pas publier cette interface si l’appareil publie l’interface de volume (définie en tant que VolumeClassGuid ou \_ volume DEVINTERFACE GUID \_ dans winioctl. h). si l’appareil publie l’Interface du Volume, il est déjà compatible avec PnP sous Windows Gestionnaire de périphériques de média.

     

    -ET/OU-

    une nouvelle sous-clé de registre pour le fournisseur de services doit être créée à l’intérieur de la sous-clé HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows Media Gestionnaire de périphériques \\ KnownDevices. Cette clé doit avoir le nom de votre fournisseur de services et doit avoir les deux entrées de valeur de Registre \_ SZ suivantes :

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   L’appareil doit avoir un paramètre d’appareil nommé WMDMSPCLSID. La valeur de ce paramètre doit être définie comme CLSID du fournisseur de services sous la forme d’une chaîne. Pour plus d’informations sur les paramètres d’appareil, consultez Paramètres de l' [appareil](device-parameters.md).

    > [!Note]  
    > La valeur du paramètre doit être le CLSID, et non le ProgID du fournisseur de services.

     

-   Le fournisseur de services de cet appareil doit implémenter l’interface IMDServiceProvider2.
-   la clé du fournisseur de services sous HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows Media Gestionnaire de périphériques \\ Plugins \\ SP \\ baname doit contenir la valeur DWORD suivante
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> </dl>

 

 




