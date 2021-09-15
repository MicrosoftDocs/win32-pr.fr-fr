---
description: configuration requise pour les Applications Windows Media DRM-Enabled
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: configuration requise pour les Applications Windows Media DRM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522029"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>configuration requise pour les Applications Windows Media DRM-Enabled

pour créer une application Windows Media Digital Rights Management (DRM), vous devez disposer des en-têtes et des bibliothèques décrits dans la section [configuration générale requise pour le développement d’applications](general-requirements-for-application-development.md) de ce document. En outre, l’application doit fournir des propriétés supplémentaires dans les informations du client lors de l’ouverture de l’appareil.

les deux propriétés supplémentaires requises pour activer les transferts de contenu protégés par DRM Windows sont décrites dans le tableau suivant.



| Propriété                                      | Description                              |
|-----------------------------------------------|------------------------------------------|
| \_ \_ \_ clé privée d’application \_ WMDRM \_ du client wpd | Spécifie la clé privée de l’application. |
| \_certificat d' \_ \_ application WMDRM du client \_ wpd  | Spécifie le certificat de l’application. |



 

Ces propriétés doivent être fournies dans les informations du client de l’application lorsque l’appareil est ouvert à l’aide de la méthode [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) . Lorsque ces propriétés sont fournies, l’API WPD autorise les transferts de contenu protégés. Si l’application a fourni un certificat et une clé privée, l’API crée un canal sécurisé pour transférer le contenu WMDRM protégé sur l’appareil.

pour plus d’informations sur la création et la distribution d’applications Windows qui prennent en charge Windows Media DRM, consultez la rubrique suivante [sur les applications basées sur les licences Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .

## <a name="transferring-content"></a>Transfert de contenu

Pour transférer le contenu protégé WMDRM, utilisez [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Cette méthode peut être utilisée pour le contenu protégé et en clair sans options supplémentaires. L’API WPD sélectionne automatiquement le canal protégé ou en clair, selon que le contenu est protégé ou désactivé. Il interagit avec le fournisseur de contenu sécurisé WMDRM pour traiter les licences WMDRM.

## <a name="transferring-known-clear-content"></a>Transfert de contenu clair connu

Si vous avez activé votre application pour gérer le contenu protégé, mais que vous savez qu’un fichier spécifique n’est pas protégé, vous pouvez indiquer à WPD d’ignorer le traitement DRM en définissant l' **option d’API WPD utiliser l’option d' \_ \_ \_ \_ effacement des \_ \_ flux de données** avec la valeur true dans le **IPortableDeviceValues** d’entrée lors de l’appel de [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) pour effacer le contenu.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Accès aux opérations de contrôle à l’aide de IWMDRMDeviceApp

WPD fournit un mécanisme permettant d’accéder aux API **IWMDRMDeviceApp** pour les mises à jour de licence et la récupération des données de contrôle. Pour accéder à cette API via WPD, appelez **QueryInterface** sur **IID \_ IWMDRMDeviceApp** à partir de l' **IStream** retourné par [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Cette instance **IWMDRMDeviceApp** est liée à la connexion **IPortableDevice** à votre appareil compatible WMDRM, et non au contenu spécifique dans lequel l' **IStream** a été obtenu. WPD encapsule en interne les API de contrôle et les rend accessibles à votre application. Votre application doit utiliser la \_ constante WMDRMDEVICEAPP use \_ wpd \_ Device \_ PTR pour le paramètre *IWMDMDevice* \* .

L’extrait de code suivant illustre cela.


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



Les mêmes prérequis avec la clé privée et le certificat de l’application s’appliquent également ici. Si la clé/le certificat n’est pas valide ou si l’initialisation du système WMDRM échoue, l’appel **QueryInferface** échoue.

La méthode ci-dessus pour acquérir l’interface **IWMDRMDeviceApp** à partir du pointeur **IStream** n’est utile que si votre application effectue déjà un transfert de contenu protégé préalablement, avant de continuer à effectuer des opérations de contrôle et de synchronisation des licences.

Notre recommandation pour la plupart des applications qui ont besoin d’accéder à **IWMDRMDeviceApp** consiste à initialiser **IWMDRMDeviceApp** directement, car cela ne nécessite pas que votre application transfère le contenu protégé ou conserve les interfaces de transfert pour effectuer la synchronisation des appareils et des licences. cette méthode nécessite l’utilisation des api Windows Media Gestionnaire de périphériques (WMDM). Pour plus d’informations et pour obtenir des exemples de code, consultez le livre blanc [accès aux API WMDRM à partir d’une application wpd](../windows-portable-devices.md) sur le site WHDC.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Windows Appareils mobiles**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
