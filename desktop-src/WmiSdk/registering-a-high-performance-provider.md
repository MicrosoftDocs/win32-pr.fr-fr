---
description: Comme les autres fournisseurs d’instances, vous inscrivez un fournisseur de haute performance auprès de Microsoft Windows&\# 160 ; Management Instrumentation (WMI) en créant une instance des \_ \_ classes Win32Provider et \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034255"
---
# <a name="registering-a-high-performance-provider"></a>Inscription d’un fournisseur de High-Performance

Comme les autres fournisseurs d’instances, vous inscrivez un fournisseur de haute performance auprès de Microsoft Windows Management Instrumentation (WMI) en créant une instance des classes [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) . L’instance **\_ \_ Win32Provider** définit l’implémentation physique du fournisseur et l’instance **\_ \_ InstanceProviderRegistration** définit l’ensemble de fonctionnalités du fournisseur. Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).

La procédure suivante décrit comment inscrire un fournisseur d’instances à hautes performances.

**Pour inscrire un fournisseur d’instances à hautes performances**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) décrivant le fournisseur.

    Veillez à ajouter une propriété **ClientLoadableCLSID** à l’instance [**\_ \_ Win32Provider**](--win32provider.md) . Si le fournisseur et le client résident sur le même ordinateur, WMI charge le fournisseur in-process sur le client à l’aide de **ClientLoadableCLSID** comme identificateur de classe. Lorsque le fournisseur et le client résident sur des ordinateurs différents, WMI charge le fournisseur in-process dans le processus WMI. WMI utilise également **ClientLoadableCLSID** pour prendre en charge les opérations d’actualisation.

2.  Créez une instance de la classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    Veillez à baliser la classe avec les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) . Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe. Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.

    Un fournisseur à hautes performances doit également indiquer la prise en charge des opérations, des opérations d’énumération ou des deux. Veillez à utiliser les propriétés **SupportsGet** et **SupportsEnumeration** dans votre implémentation.

L’exemple de code suivant montre comment implémenter les classes [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) pour un fournisseur à hautes performances.

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



