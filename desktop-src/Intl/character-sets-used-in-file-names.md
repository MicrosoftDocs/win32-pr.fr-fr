---
description: NTFS stocke les noms de fichiers au format Unicode. En revanche, les anciens systèmes de fichiers FAT12, FAT16 et FAT32 utilisent le jeu de caractères OEM. Pour plus d'informations, consultez Pages de codes.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Jeux de caractères utilisés dans les noms de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad9033b3ea723de757c59a73fc62c91a56da286ca74ca7444f31db42ff539f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107379"
---
# <a name="character-sets-used-in-file-names"></a>Jeux de caractères utilisés dans les noms de fichiers

NTFS stocke les noms de fichiers au format Unicode. En revanche, les anciens systèmes de fichiers FAT12, FAT16 et FAT32 utilisent le jeu de caractères OEM. Pour plus d’informations, consultez [Pages de codes](code-pages.md).

les applications Non-Unicode qui créent des fichiers FAT doivent parfois utiliser les fonctions de conversion de la bibliothèque runtime C standard pour effectuer la conversion entre le jeu de caractères de la page de codes Windows et le jeu de caractères de la page de codes OEM. Avec les implémentations Unicode des fonctions du système de fichiers, il n’est pas nécessaire d’effectuer de telles traductions.

votre application peut utiliser des types de chaîne génériques, comme décrit dans [Windows types de données pour les chaînes](windows-data-types-for-strings.md). L’application peut également utiliser des prototypes de fonctions génériques à l’aide de techniques décrites dans [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md). Pour les types de chaîne génériques ou les prototypes de fonction génériques, votre application peut utiliser un fichier source unique pour compiler une version Unicode ou non-Unicode. Pour ce faire, l’application fournit des macros pour les fonctions qui ne sont pas appelées lors de la compilation pour Unicode.

Dans les systèmes de fichiers NTFS et FAT, les caractères spéciaux sont les suivants : ' \\ ', '/', '. ', ' ? 'et' \* '. Sur les pages de codes OEM, ces caractères spéciaux se trouvent dans la plage de caractères ASCII (0x00 à 0x7F). Leurs équivalents Unicode ont les mêmes valeurs dans une forme de 2 octets, 0x0000 à 0x007F.

> [!Caution]  
> Windows page de codes et les jeux de caractères de la page de codes OEM utilisés sur les systèmes d’exploitation en langue japonaise contiennent le symbole Yen (¥) au lieu d’une barre oblique inverse ( \\ ). Ainsi, le symbole yen est un caractère interdit pour les systèmes de fichiers NTFS et FAT. Lors du mappage Unicode sur une page de codes de langue japonaise, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) et d’autres fonctions de conversion mappent la barre oblique inverse (u + 005C) et le symbole de yen Unicode normal (u + 00A5) sur ce même caractère. Pour des raisons de sécurité, les applications ne doivent pas, en général, autoriser le caractère U + 00A5 dans une chaîne Unicode qui peut être convertie pour être utilisée comme nom de fichier FAT. Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> <dt>

[Considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md)
</dt> </dl>

 

 



