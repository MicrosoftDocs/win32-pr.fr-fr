---
description: Pour NLS, le tri (également connu sous le nom de &\# 0034 ; collation&\# 0034 ;) est la disposition des chaînes.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Tri (internationalisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130209"
---
# <a name="sorting"></a>Tri

Pour NLS, le tri (également appelé « classement ») est la disposition des chaînes. Il existe deux types de tri :

-   Tri linguistique. Réorganise les chaînes avec des caractéristiques linguistiques similaires en groupes (par tris).
-   Tri ordinal (non linguistique). Réorganise les chaînes dans une séquence ordonnée.

Le tri utilise les fonctions de comparaison de chaînes NLS, telles que [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), ou les fonctions d’API « Wrapper », telles que [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), qui appellent en interne les fonctions de comparaison de chaînes nls.

Pour plus d’informations sur l’implémentation du tri dans vos applications, consultez [gestion du tri dans vos applications](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la prise en charge linguistique nationale](about-national-language-support.md)
</dt> <dt>

[Gestion du tri dans vos applications](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
