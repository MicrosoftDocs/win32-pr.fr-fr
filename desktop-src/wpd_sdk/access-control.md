---
description: Contrôle d’accès
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83caa01b08409afd196ea0507cb47986928a1d947b6ff7907640e4f9bd5b390f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657909"
---
# <a name="access-control-wpd-api"></a>Access Control (API WPD)

le Windows Driver Model (WDM) prend en charge la restriction de l’accès des appareils via les listes de Access Control (acl) sur les nœuds de l’appareil Plug-and-Play (PnP). Cela signifie que les fournisseurs et les administrateurs réseau peuvent restreindre l’accès à n’importe quel type d’appareil. Lorsqu’une application ouvre un handle à un pilote en appelant [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), le gestionnaire d’e/s du pilote vérifie si l’utilisateur donné dispose de l’accès requis, et effectue de la même manière des contrôles d’accès lorsque les IOCTL sont envoyées au pilote à partir de ce handle.

Par exemple, un administrateur réseau peut restreindre les utilisateurs invités à l’accès en lecture seule pour les périphériques portables, alors qu’ils peuvent accorder aux utilisateurs authentifiés un accès en lecture/écriture. Dans ce cas, cela implique que si un invité a émis une commande WPD nécessitant un accès en lecture/écriture (par exemple, supprimer un objet); elle échoue avec l’accès refusé, tandis que si un utilisateur authentifié a émis la même commande, elle réussit.

Les entrées de stratégie de groupe pour le contrôle de l’accès au stockage amovible et aux périphériques portables ne sont en fait rien de plus qu’un moyen simple pour les administrateurs d’appliquer des ACL de nœuds de périphérique PnP à une classe entière d’appareils à la fois (par exemple, en appliquant l’autorisation « refuser l’accès en écriture aux périphériques portables stratégie de groupe ».

## <a name="io-control-codes-in-wpd"></a>Codes de contrôle d’e/s dans WPD

Les applications WPD communiquent avec les pilotes en ouvrant des descripteurs d’appareil et en envoyant des codes de contrôle d’e/s (IOCTL). Ces IOCTL se composent de quatre sections :

1.  Type d’appareil
2.  Code de fonction
3.  Buffer, méthode
4.  Type d’accès

La quatrième section, le type d’accès, spécifie la spécification d’accès spécifique pour la commande donnée. Le gestionnaire d’e/s du pilote utilise ces données pour effectuer la vérification de la liste de Access Control (ACL).

Par conséquent, si une IOCTL a été définie comme :


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



Le gestionnaire d’e/s du pilote vérifie que le propriétaire du descripteur de l’appareil dispose d’un accès en lecture à l’appareil lorsque ce message est envoyé.

Et, si une IOCTL a été définie comme :


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



Le gestionnaire d’e/s du pilote vérifie que le propriétaire du descripteur de l’appareil dispose d’un accès en lecture/écriture à l’appareil lorsque ce message est envoyé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’application**](application-overview.md)
</dt> <dt>

[**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



