---
title: Pages de codes et chaînes Unicode
description: Un autre point à prendre en compte dans l’implémentation de IPropertySetStorage est la façon dont les noms de propriété Unicode sont stockés dans l’ID de propriété 0 (le dictionnaire de noms de propriétés), qui n’utilise pas de chaînes Unicode.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Pages de codes et chaînes Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a1d5a830d3d4e2fccbb61563e7a8a0447d74e7c427e5e2e0434e7194a2ad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663599"
---
# <a name="code-pages-and-unicode-strings"></a>Pages de codes et chaînes Unicode

Un autre point à prendre en compte dans l’implémentation de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) est la façon dont les noms de propriété Unicode sont stockés dans l’ID de propriété 0 (le dictionnaire de noms de propriétés), qui n’utilise pas de chaînes Unicode.

Unicode a officiellement une valeur de page de codes de 1200. Pour stocker des valeurs Unicode dans le dictionnaire de noms de propriétés, utilisez la valeur de page de codes 1200 pour le jeu de propriétés entier (dans l’ID de propriété 1), spécifié par l’absence de l’indicateur **\_ ANSI PROPSETFLAG** dans [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). N’oubliez pas que cela a pour effet secondaire de stocker toutes les valeurs de chaîne dans le jeu de propriétés Unicode. Dans toutes les pages de codes, le nombre trouvé au début d’un **VT de VT \_** est un nombre d’octets, et non un nombre de caractères. Cela est nécessaire pour assurer la compatibilité avec les clients de version antérieure.

L’implémentation de fichier composé de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crée tous les nouveaux jeux de propriétés entièrement en Unicode (page de codes 1200) ou dans la page de codes ANSI du système en cours. Cela est contrôlé par l’absence ou la présence de l’indicateur **\_ ANSI PROPSETFLAG** dans le paramètre *grfFlags* de [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).

Créez et ouvrez les jeux de propriétés au format Unicode. Pour l’implémenter, ne définissez pas l’indicateur **\_ ANSI PROPSETFLAG** dans le paramètre *grfFlags* de [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Évitez d’utiliser les valeurs **VT \_ LPSTR** et utilisez à la place des valeurs **VT \_ LPWStr** . Lorsque la page de codes du jeu de propriétés est Unicode, les valeurs de chaîne de **VT \_ LPSTR** sont converties au format Unicode lorsqu’elles sont stockées, et reviennent aux valeurs de chaîne multioctets lors de leur récupération.

La définition de l’indicateur **\_ ANSI PROPSETFLAG** comme signalé par un appel à [**IPropertyStorage :: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) indique si la page de codes sous-jacente est ou n’est pas au format Unicode. N’oubliez pas que l’ID de propriété 1 peut être lu de manière explicite pour apprendre la page de codes.

Vous pouvez accéder à l’ID de propriété 1 à l’aide d’un appel à [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Toutefois, il est en lecture seule et ne peut pas être mis à jour avec [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). En outre, il ne peut pas être supprimé avec [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple).

 

 




