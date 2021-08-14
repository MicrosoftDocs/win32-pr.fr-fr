---
title: Co-Branding des magasins en ligne
description: Co-Branding des magasins en ligne
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Lecteur Windows Media magasins en ligne, co-personnalisation
- magasins en ligne, co-personnalisation
- tapez 1 magasins en ligne, co-personnalisation
- tapez 2 magasins en ligne, co-personnalisation
- Co-personnalisation des magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3ca69c377a7aedeb71f05008d707fab955f02bf0e02d7b0ca35861105aade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342130"
---
# <a name="co-branding-online-stores"></a>Co-Branding des magasins en ligne

Les fabricants d’ordinateurs personnels qui ne fonctionnent pas avec un magasin de musique peuvent cohabiter avec les fournisseurs de magasins en ligne. Lecteur Windows Media le programme d’installation prend en charge le paramètre de ligne de commande ServiceExtra pour permettre aux oem de matériel de définir un attribut personnalisé que le magasin en ligne peut utiliser pour identifier le fabricant OEM qui a installé le magasin en ligne initial.

par exemple, si un créateur d’ordinateur nommé Fabrikam souhaite définir le magasin en ligne initial sur le magasin de musique proseware, il peut utiliser la ligne de commande suivante pour installer Lecteur Windows Media 10 :


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



lorsque Lecteur Windows Media est installé de cette manière, le lecteur ajoute la chaîne ServiceExtra chaque fois qu’il ouvre le service proseware. l’exemple suivant montre l’URL que Lecteur Windows Media envoie au service proseware pour récupérer le document ServiceInfo :


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



le magasin en ligne proseware peut ensuite utiliser la chaîne de requête pour déterminer quel OEM a installé Lecteur Windows Media et retourner un document ServiceInfo généré dynamiquement qui pointe vers la version comarquée du magasin en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Paramètres de ligne de commande d’installation pour les magasins en ligne**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




