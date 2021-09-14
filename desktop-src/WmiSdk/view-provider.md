---
description: Le fournisseur d’affichage est une instance et un fournisseur de méthode qui crée des classes basées sur des instances d’autres classes.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Fournisseur de vues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855567"
---
# <a name="view-provider"></a>Fournisseur de vues

Le fournisseur d’affichage est une instance et un fournisseur de méthode qui crée des classes basées sur des instances d’autres classes. Vous pouvez utiliser le fournisseur d’affichage pour prendre des propriétés à partir de différentes classes sources, d’espaces de noms différents ou de différents ordinateurs et combiner les propriétés en tant que classe unique.

En tant que fournisseur d’instance et de méthode, le fournisseur de vue prend en charge l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard et les méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) suivantes :

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Pour plus d’informations sur les qualificateurs utilisés pour définir des classes de fournisseur d’affichage, consultez [qualificateurs spécifiques au fournisseur de vues](qualifiers-specific-to-the-view-provider.md).

Pour plus d’informations sur les affichages, consultez [liaison de classes](linking-classes-together.md).

Deux versions du fournisseur d’affichages sont disponibles sur les plateformes 64 bits. Pour plus d’informations, consultez [obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).

Le fournisseur d’affichage est implémenté dans ViewProv.dll.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> </dl>

 

 



