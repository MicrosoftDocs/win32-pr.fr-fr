---
description: NLS comprend un certain nombre de fonctions API que vos applications peuvent utiliser pour mapper les données de paramètres régionaux entre les identificateurs de paramètres régionaux et les noms de paramètres régionaux, et répertorier les paramètres régionaux neutres.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mappage des données de paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239969"
---
# <a name="mapping-locale-data"></a>Mappage des données de paramètres régionaux

NLS comprend un certain nombre de fonctions API que vos applications peuvent utiliser pour mapper les données de paramètres régionaux entre les [identificateurs](locale-identifiers.md) de paramètres régionaux et les [noms de paramètres régionaux](locale-names.md), et répertorier les paramètres régionaux neutres. cette rubrique traite de l’utilisation de ces fonctions sur Windows vista et versions ultérieures, ainsi que sur les systèmes d’exploitation antérieurs à Windows vista (parfois appelés « systèmes de niveau inférieur »).

## <a name="map-locale-data-on-windows-vista-and-later"></a>mapper les données de paramètres régionaux sur Windows Vista et versions ultérieures

NLS fournit plusieurs fonctions de mappage de paramètres régionaux utilisables par les applications que vous développez pour s’exécuter sur Windows Vista et versions ultérieures. Il comprend également les fonctions que vos applications peuvent utiliser pour énumérer les paramètres régionaux neutres.

**Utiliser les fonctions de conversion standard pour le mappage de données**

Pour effectuer un mappage entre un nom de paramètres régionaux et un identificateur de paramètres régionaux, votre application peut appeler la fonction [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) . L’application utilise [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) pour effectuer un mappage entre un identificateur de paramètres régionaux et un nom de paramètres régionaux.

**Répertorier les paramètres régionaux neutres**

pour énumérer les paramètres régionaux neutres pour Windows 7 et versions ultérieures, votre application peut appeler [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) avec *dwFlags* défini sur [**locale \_ NEUTRALDATA**](locale-neutraldata.md). Elle peut également utiliser [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec *LCTYPE* défini sur [**locale \_ INEUTRAL**](locale-ineutral.md).

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>mapper les données de paramètres régionaux sur les systèmes d’exploitation antérieurs à Windows Vista

NLS comprend une bibliothèque de liens directs (DLL) à utiliser pour les applications que vous développez pour s’exécuter sur les systèmes d’exploitation antérieurs à Windows Vista. La DLL prend en charge les fonctions de conversion et de liste pour le mappage des données.

> [!Note]  
> les Applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures ne doivent pas utiliser les fonctions de mappage ou d’énumération de niveau inférieur.

 

**Utiliser les fonctions de conversion de niveau inférieur pour le mappage de données**

Votre application ciblée sur un système de bas niveau peut appeler la fonction [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) pour convertir un identificateur de paramètres régionaux en un nom de paramètres régionaux. S’il doit convertir un nom de paramètres régionaux en un identificateur de paramètres régionaux, il doit appeler [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).

**Utiliser les fonctions de la liste de bas niveau pour énumérer les paramètres régionaux neutres**

Votre application doit appeler [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) pour récupérer l’identificateur de paramètres régionaux du parent pour des paramètres régionaux. Si l’application doit obtenir le nom des paramètres régionaux du parent pour les paramètres régionaux, elle doit appeler [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Identificateurs de paramètres régionaux](locale-identifiers.md)
</dt> <dt>

[Noms de paramètres régionaux](locale-names.md)
</dt> </dl>

 

 



