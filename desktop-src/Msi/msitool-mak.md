---
description: Msitool. Mak est un Makefile que vous pouvez utiliser pour générer des outils et des actions personnalisées.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool. Mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021308"
---
# <a name="msitoolmak"></a>Msitool. Mak

Msitool. Mak est un Makefile que vous pouvez utiliser pour générer des outils et des actions personnalisées. Il peut être utilisé avec Visual C++ version 4,0 ou ultérieure. Pour plus d’informations, consultez le fichier d’en-tête. Un ensemble de valeurs doit être défini avant d’inclure ce fichier. En général, les développeurs placent ceux-ci au début du. cpp, ifdef devant être ignorés par le compilateur C. De même, les ressources sont ajoutées à la fin du fichier. cpp. Pour plus d’informations, consultez les exemples.

VCBIN peut être défini dans le répertoire où se trouvent les outils de Visual C++ ou le Makefile utilise MSVCDIR et MSDEVDIR. Si ces derniers ne sont pas définis, ils ne spécifient pas d’emplacement, en supposant que les outils se trouvent sur le chemin d’accès. Un problème avec les variables d’environnement dans Visual C++ version 5,0 est que si les deux ne se trouvent pas sur votre chemin d’accès, l’éditeur de liens ne trouve pas Msdis100.dll. Si vous la copiez à partir de MSDEVDIR vers MSVCDIR, cela fonctionne. L’autre option consiste à copier Msdis100.dll et Rc.exe et Rcdll.dll vers MSVCDIR, et à définir VCBIN sur ce.

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



