---
description: Considérations relatives à la programmation pour l’utilisation des liens symboliques.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considérations relatives à la programmation (systèmes de fichiers locaux)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a98c244dac3fb4a9f6b73d11067af64512e0cfd54e58078bd87a2582b0c2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981879"
---
# <a name="programming-considerations-local-file-systems"></a>Considérations relatives à la programmation (systèmes de fichiers locaux)

Gardez à l’esprit les considérations de programmation suivantes lorsque vous utilisez des liens symboliques :

-   Les liens symboliques peuvent pointer vers une cible inexistante.
-   Lorsque vous créez un lien symbolique, le système d’exploitation ne vérifie pas si la cible existe.
-   Si une application tente d’ouvrir une cible inexistante, **le \_ fichier d’erreur \_ \_ introuvable** est retourné.
-   Les liens symboliques sont des points d’analyse. Pour plus d’informations, consultez [déterminer si un répertoire est un dossier monté](determining-whether-a-directory-is-a-volume-mount-point.md).
-   Il y a un maximum de 63 points d’analyse (et par conséquent des liens symboliques) autorisés dans un chemin d’accès particulier.

    **Windows Server 2003 et Windows XP :** Il existe une limite de 31 points d’analyse sur un chemin d’accès donné.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>


</dt> <dt>

[Liens physiques et jonctions](hard-links-and-junctions.md)
</dt> </dl>

 

 



