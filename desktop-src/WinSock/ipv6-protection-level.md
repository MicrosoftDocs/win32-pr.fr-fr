---
description: L' \_ option de socket de niveau de protection IPv6 permet aux \_ développeurs de placer des restrictions d’accès sur les sockets IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfdd456bd6c04819547f61a70b2df960cdd494b6d651d56a0f811d44bf636a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112093"
---
# <a name="ipv6_protection_level"></a>\_Niveau de protection IPv6 \_

L' \_ option de socket de niveau de protection IPv6 permet aux \_ développeurs de placer des restrictions d’accès sur les sockets IPv6. Ces restrictions permettent à une application qui s'exécute sur un réseau local privé de se renforcer facilement et efficacement contre les attaques externes. L' \_ \_ option de socket de niveau de protection IPv6 élargit ou limite l’étendue d’un socket d’écoute, en permettant l’accès illimité des utilisateurs publics et privés, le cas échéant, ou en limitant l’accès au même site, selon les besoins.

Le \_ niveau de protection IPv6 \_ a actuellement trois niveaux de protection définis.



| Niveau de protection                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>niveau de PROTECTION non \_ \_ restreint<br/>       | utilisé par les applications conçues pour fonctionner sur Internet, y compris les applications tirant parti des fonctionnalités de traversée NAT IPv6 intégrées à Windows (Teredo, par exemple). Ces applications peuvent contourner les pare-feux IPv4 ; elles doivent donc être renforcées contre les attaques Internet dirigées sur le port ouvert.<br/> |
| <span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>niveau de PROTECTION \_ \_ EDGERESTRICTED<br/> | Utilisé par les applications conçues pour fonctionner sur Internet. ce paramètre n’autorise pas la traversée NAT à l’aide de l’implémentation Windows Teredo. Ces applications peuvent contourner les pare-feux IPv4 ; elles doivent donc être renforcées contre les attaques Internet dirigées sur le port ouvert.<br/>                                   |
| <span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>niveau de PROTECTION \_ \_ restreint<br/>             | Utilisé par les applications intranet qui n’implémentent pas les scénarios Internet. Ces applications ne sont généralement pas testées ou renforcées contre les attaques Internet.<br/> Ce paramètre limitera uniquement le trafic reçu aux liens locaux.<br/>                                                                             |



 

L’exemple de code suivant fournit les valeurs définies pour chaque :

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

Ces valeurs s’excluent mutuellement et ne peuvent pas être combinées dans un seul appel de fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Les autres valeurs de cette option de socket sont réservées. Ces niveaux de protection s’appliquent uniquement aux connexions entrantes. La définition de cette option de socket n’a aucun effet sur les paquets sortants ou les connexions.

sur Windows 7 et Windows Server 2008 R2, la valeur par défaut pour le \_ niveau de protection ipv6 n’est pas spécifiée et le niveau de \_ **protection \_ \_ par défaut** est défini sur-1, une valeur non autorisée pour le \_ niveau de protection ipv6 \_ .

sur Windows Vista et Windows Server 2008, la valeur par défaut du niveau de protection ipv6 \_ \_ est **niveau de protection non \_ \_ restreint** et le **niveau de protection \_ \_ par défaut** est défini sur-1, une valeur non autorisée pour le \_ niveau de protection ipv6 \_ .

sur Windows Server 2003 et Windows XP, la valeur par défaut pour le niveau de protection IPV6 est le niveau de protection EDGERESTRICTED et le niveau de protection \_ \_ **\_ \_ par défaut** est défini sur le **niveau de protection \_ \_ EDGERESTRICTED**. **\_ \_**

> [!Note]  
> L' \_ option de socket de niveau de protection IPv6 \_ doit être définie avant que le socket ne soit lié. Dans le cas contraire, les paquets reçus entre les appels [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) sont conformes au **niveau de protection \_ \_ EDGERESTRICTED** et peuvent être remis à l’application.

 

Le tableau suivant décrit l’effet de l’application de chaque niveau de protection à un socket d’écoute.

Niveau de protection

Trafic entrant autorisé

Même site

Externe

Parcours NAT (Teredo)

niveau de PROTECTION \_ \_ restreint

Oui

Non

Non

niveau de PROTECTION \_ \_ EDGERESTRICTED

Oui

Oui

Non

niveau de PROTECTION non \_ \_ restreint

Oui

Oui

Oui



 

Dans le tableau ci-dessus, la même colonne de **site** est une combinaison des éléments suivants :

-   Lier des adresses locales
-   Adresses locales du site
-   Adresses globales connues pour appartenir au même site (correspondant à la table de préfixe de site)

sur Windows 7 et Windows Server 2008 R2, la valeur par défaut pour le \_ niveau de PROTECTION IPV6 \_ n’est pas spécifiée. si aucun logiciel de pare-feu prenant en charge la traversée latérale n’est installé sur l’ordinateur local (Windows pare-feu est désactivé ou si un autre pare-feu est installé et ignore le trafic teredo), vous recevrez le trafic teredo uniquement si vous définissez l' \_ \_ option de socket de niveau de protection IPV6 sur **niveau de protection non \_ \_ restreint**. toutefois, Windows pare-feu ou toute stratégie de pare-feu prenant en charge la traversée latérale peut ignorer cette option en fonction des paramètres de stratégie du pare-feu. En définissant cette option de socket sur **niveau de protection \_ \_ sans restriction**, l’application communique son intention explicite de recevoir le trafic traversé par le pare-feu hôte installé sur l’ordinateur local. Par conséquent, si un pare-feu hôte prenant en charge la traversée latérale est installé, il aura la décision finale d’accepter un paquet. Par défaut, sans option de socket définie :

-   o si Windows pare-feu est activé (ou qu’un autre pare-feu d’hôte prenant en charge la traversée latérale est installé) sur l’ordinateur local, tout ce qu’il impose est observé. Le pare-feu d’hôte prenant en charge la traversée latérale standard bloquera le trafic Teredo par défaut. Par conséquent, les applications observent la valeur par défaut comme s’il s’agissait d’un **niveau de protection \_ \_ EDGERESTRICTED**.
-   o si Windows pare-feu n’est pas activé et qu’aucun autre pare-feu d’hôte prenant en charge la traversée latérale n’est installé sur le système local, le niveau de PROTECTION par défaut est **\_ \_ EDGERESTRICTED**.

sur Windows Vista et Windows Server 2008, la valeur par défaut du niveau de protection IPV6 \_ \_ est **niveau de protection non \_ \_ restreint**. mais la valeur effective varie selon que Windows pare-feu est activé. le pare-feu Windows prend en charge la traversée de périphérie (prise en charge de Teredo), quelle que soit la valeur définie pour le \_ niveau de protection ipv6 \_ et ignore si le niveau de protection ipv6 est sans \_ \_ **\_ \_ restriction**. La valeur effective dépend de la stratégie de pare-feu. lorsque Windows pare-feu est désactivé et qu’aucun autre pare-feu prenant en charge la traversée latérale n’est installé sur l’ordinateur local, la valeur par défaut du niveau de protection IPV6 \_ \_ est **niveau de protection non \_ \_ restreint**.

sur Windows Server 2003 et Windows XP, la valeur par défaut pour le \_ niveau de protection IPV6 \_ est niveau de **protection \_ \_ EDGERESTRICTED**. À moins que vous n’ayez défini l' \_ \_ option de socket de niveau de protection IPv6 sur **niveau de protection non \_ \_ restreint**, vous ne recevrez pas de trafic Teredo.

Selon le \_ niveau de protection IPv6 \_ , une application qui nécessite un trafic non sollicité provenant d’Internet peut ne pas être capable de recevoir du trafic non sollicité. toutefois, ces exigences ne sont pas nécessaires pour recevoir le trafic sollicité sur le Windows interface Teredo. Pour plus d’informations sur l’interaction avec Teredo, consultez [réception du trafic sollicité sur Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).

Lorsque des paquets entrants ou des connexions sont refusés en raison du niveau de protection défini, le rejet est géré comme si aucune application n’était à l’écoute sur ce Socket.

> [!Note]
>
> l' \_ \_ option de socket de niveau de PROTECTION ipv6 ne place pas nécessairement les restrictions d’accès sur les sockets ipv6 ou ne restreint pas la traversée NAT à l’aide d’une méthode autre que Windows teredo, ou même en utilisant une autre implémentation de teredo par un autre fournisseur.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[Réception du trafic sollicité sur Teredo](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
