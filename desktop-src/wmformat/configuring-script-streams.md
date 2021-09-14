---
title: Configuration des Flux de script
description: Configuration des Flux de script
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flux, configuration de flux de script
- codecs, configuration de flux de script
- flux de script, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219601"
---
# <a name="configuring-script-streams"></a>Configuration des Flux de script

Comme tous les types de flux arbitraires, les flux de script doivent avoir une fenêtre de mémoire tampon et une vitesse de transmission définies pour eux. Le type de média majeur dans la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) doit être défini sur WMMEDIATYPE \_ script.

Les flux de script doivent avoir le membre **formatType** du **\_ \_ type de média WM** défini sur WMFORMAT \_ script, qui indique que le membre **pbFormat** pointe vers une structure [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .

Il n’existe qu’un seul type de script pris en charge, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les Flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Commandes de script**](script-commands.md)
</dt> </dl>

 

 




