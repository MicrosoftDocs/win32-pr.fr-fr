---
title: Co-Branding des magasins en ligne
description: Co-Branding des magasins en ligne
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Online stores, co-personnalisation
- magasins en ligne, co-personnalisation
- tapez 1 magasins en ligne, co-personnalisation
- tapez 2 magasins en ligne, co-personnalisation
- Co-personnalisation des magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512045"
---
# <a name="co-branding-online-stores"></a>Co-Branding des magasins en ligne

Les fabricants d’ordinateurs personnels qui ne fonctionnent pas avec un magasin de musique peuvent cohabiter avec les fournisseurs de magasins en ligne. Le programme d’installation du lecteur Windows Media prend en charge le paramètre de ligne de commande ServiceExtra pour permettre aux OEM de matériel de définir un attribut personnalisé que le magasin en ligne peut utiliser pour identifier le fabricant OEM qui a installé le magasin en ligne initial.

Par exemple, si un créateur d’ordinateur nommé Fabrikam souhaite définir le magasin en ligne initial sur le magasin de musique Proseware, il peut utiliser la ligne de commande suivante pour installer le lecteur Windows Media 10 :


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Lorsque le lecteur Windows Media est installé de cette manière, le lecteur ajoute la chaîne ServiceExtra chaque fois qu’il ouvre le service proseware. L’exemple suivant montre l’URL que le lecteur Windows Media envoie au service Proseware pour récupérer le document ServiceInfo :


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



Le magasin en ligne Proseware peut ensuite utiliser la chaîne de requête pour déterminer quel OEM a installé le lecteur Windows Media et retourner un document ServiceInfo généré dynamiquement qui pointe vers la version comarquée du magasin en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Paramètres de ligne de commande d’installation pour les magasins en ligne**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




