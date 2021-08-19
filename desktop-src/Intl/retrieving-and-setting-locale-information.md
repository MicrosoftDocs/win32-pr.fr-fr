---
description: Récupération et définition des informations relatives aux paramètres régionaux
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Récupération et définition des informations relatives aux paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d02c2bb58328529781309ce8284310acbcb6fb545ecdc076df295cd020344a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130309"
---
# <a name="retrieving-and-setting-locale-information"></a>Récupération et définition des informations relatives aux paramètres régionaux

L’application doit être en mesure de récupérer et de définir des informations spécifiques sur [les paramètres régionaux et les langues](locales-and-languages.md)disponibles. Chaque élément d’informations de paramètres régionaux, tel que le nom d’un jour spécifique de la semaine ou le caractère utilisé comme séparateur décimal, a une constante correspondante. Les constantes disponibles sont définies dans les [constantes d’informations de paramètres régionaux](locale-information-constants.md).

Votre application stocke et manipule toujours les informations de paramètres régionaux comme une chaîne terminée par le caractère null. Aucune donnée binaire n’est autorisée, et toutes les valeurs numériques doivent être spécifiées en tant que texte. Chaque type d’informations a un format particulier. En outre, plusieurs types sont liés entre eux afin que la modification d’un type modifie également la valeur de l’autre type.

Pour récupérer les informations relatives aux paramètres régionaux, l’application appelle [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante qui correspond aux informations requises. L’application peut appeler [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) pour définir un élément d’informations de paramètres régionaux.

> [!Note]  
> Bien qu’un [identificateur de paramètres régionaux](locale-identifiers.md) soit pris en charge, il n’est pas disponible pour une application, sauf si les paramètres régionaux correspondants sont également installés.

 

Étant donné que la plupart des constantes d’informations de paramètres régionaux sont mutuellement exclusives, un seul type d’informations peut être géré à la fois. Les exceptions à cette règle sont les [paramètres régionaux \_ use \_ CP \_ ACP](locale-use-cp-acp.md), [locale \_ \_ Number Number](locale-return-constants.md)et [locale \_ NOUSEROVERRIDE](locale-nouseroverride.md), qui peuvent être combinés avec d’autres constantes à l’aide d’un fichier binaire ou.

> [!Caution]  
> L’utilisation de paramètres régionaux \_ NOUSEROVERRIDE est fortement déconseillée, car elle désactive les préférences de l’utilisateur.

 

Comme un certain nombre d’applications, par exemple Microsoft Active Directory, votre application peut conserver ses chaînes dans une base de données pouvant être triée. Pour plus d’informations, consultez [gestion du tri dans vos applications](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Constantes d’informations de paramètres régionaux](locale-information-constants.md)
</dt> <dt>

[Gestion du tri dans vos applications](handling-sorting-in-your-applications.md)
</dt> <dt>

[Utilisation de paramètres régionaux personnalisés](working-with-custom-locales.md)
</dt> </dl>

 

 



