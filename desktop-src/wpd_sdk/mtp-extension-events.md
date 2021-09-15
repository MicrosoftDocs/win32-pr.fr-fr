---
description: Événements d’extension MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Événements d’extension MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522956"
---
# <a name="mtp-extension-events"></a>Événements d’extension MTP

Les événements signalent à une application que des modifications ont été apportées sur un appareil ou avec celui-ci. Par exemple, une application peut s’inscrire pour recevoir notifications qu’un appareil a été supprimé.

## <a name="vendor-extended-event-codes"></a>Fournisseurs-codes d’événements étendus

Lorsqu’un fabricant d’appareils prend en charge un événement étendu par un fournisseur, son pilote combine le code d’événement du fournisseur (UINT16) et les 16 bits les plus élevés du GUID des **\_ \_ \_ \_ \_ événements étendus du fournisseur** d’événements MTP.

Par exemple, si le code étendu du fournisseur est 0xC001, le GUID résultant est comme indiqué dans l’exemple suivant :


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Paramètres d’événement étendus du fournisseur

Les paramètres d’un événement étendu par le fournisseur sont signalés par le GUID d' **ID d’événement du \_ paramètre d’événement \_ \_ \_ wpd** et par la **propriété wpd paramètres d' \_ \_ \_ événement MTP ext \_ \_**, qui est une collection de **PROPVARIANTS**. Ces **PROPVARIANTS** correspondent aux paramètres d’événement. S’il n’y a aucun paramètre, cette collection est vide.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge des extensions MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



