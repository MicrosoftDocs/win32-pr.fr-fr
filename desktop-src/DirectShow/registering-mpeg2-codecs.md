---
description: Inscription des codecs MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Inscription des codecs MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7aaf683d03f529e394fe7e01af8ccae0e0fd009ad7a90b608c8bbebf834c5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952138"
---
# <a name="registering-mpeg2-codecs"></a>Inscription des codecs MPEG2

cette rubrique s’applique à Windows XP édition Media Center uniquement.

Windows XP Media Center Edition gère deux clés de registre qu’il utilise pour déterminer le codec à utiliser pour lire les fichiers audio et vidéo MPEG2. La première clé de Registre spécifie le codec MPEG2 préféré du fabricant de l’ordinateur, et la seconde répertorie tous les codecs compatibles Media Center qui sont actuellement installés sur l’ordinateur. Quand Media Center doit lire un fichier MPEG2, il utilise le codec préféré du fabricant, si celui-ci est spécifié. Si ce n’est pas le cas, il utilise le premier codec compatible Media Center listé dans le registre. si le registre ne spécifie aucun codec préféré ou compatible, Media Center utilise le filtre de DirectShow standard pour choisir un codec.

Pour vous assurer que Media Center utilise toujours un codec MPEG2 compatible, les fabricants d’ordinateurs Media Center doivent spécifier le codec MPEG2 préféré à l’emplacement de Registre suivant :


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



Les données de la clé doivent être les suivantes :


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Le programme d’installation d’un codec MPEG2 compatible avec Media Center doit inscrire le codec en créant deux instances de la clé de Registre suivante : une pour le codec vidéo et une pour le codec audio :


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



Les données de la clé doivent être les suivantes :


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



