---
description: Les applications clientes et les scripts qui accèdent aux fournisseurs standard WMI 32 bits continuent de fonctionner normalement lorsqu’ils s’exécutent sur un système d’exploitation 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obtention et fourniture de données sur un ordinateur 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46163290d1212fd66bef48dba177034769360e8d7c6249dfdf40327ce2adc32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819376"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Obtention et fourniture de données sur un ordinateur 64 bits

Les applications clientes et les scripts qui accèdent aux fournisseurs standard WMI 32 bits continuent de fonctionner normalement lorsqu’ils s’exécutent sur un système d’exploitation 64 bits. Seuls deux fournisseurs préinstallés, le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) et le [fournisseur de vues](view-provider.md), ont des versions 64 bits qui s’exécutent côte à côte avec les versions 32 bits. toutefois, une application 32 bits qui demande des instances de Windows Driver Model de 32 bits reçoit les instances de classe wdm 64 bits par défaut sur un système d’exploitation 64 bits.

## <a name="accessing-default-and-nondefault-provider-data"></a>Accès aux données de fournisseur par défaut et par défaut

En règle générale, les writers de fournisseur n’incluent pas les versions 32 bits et 64 bits d’un fournisseur dans le même système d’exploitation. S’il n’existe aucun fournisseur 64 bits, un fournisseur 32 bits peut continuer à s’exécuter via les fonctionnalités de WOW64. Un fournisseur 64 bits peut également fournir des données à une application 32 bits. Pour plus d’informations, consultez [fourniture de données WMI sur une plateforme 64 bits](providing-wmi-data-on-a-64-bit-platform.md).

Si deux versions existent, les applications clientes et les scripts peuvent utiliser les paramètres de contexte disponibles dans l' [API com](com-api-for-wmi.md) et l' [API de script](scripting-api-for-wmi.md) pour se connecter explicitement à un fournisseur WMI non par défaut spécifique, s’il est disponible. Pour plus d’informations, consultez [demande de données WMI sur une plateforme 64 bits](requesting-wmi-data-on-a-64-bit-platform.md).

Le diagramme suivant montre les connexions par défaut et par défaut, en utilisant le registre comme exemple pour lequel deux fournisseurs peuvent coexister côte à côte sur une plateforme 64 bits.

![connexions par défaut et par défaut sur une plateforme 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande de données WMI sur une plateforme 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fourniture de données WMI sur une plateforme 64 bits](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
