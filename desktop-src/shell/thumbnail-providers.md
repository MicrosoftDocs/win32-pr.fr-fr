---
description: Windows Vista utilise plus d’images miniatures spécifiques aux fichiers que les versions antérieures de Windows.
title: Gestionnaires de miniatures
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196383"
---
# <a name="thumbnail-handlers"></a>Gestionnaires de miniatures

Windows Vista utilise plus d’images miniatures spécifiques aux fichiers que les versions antérieures de Windows. Windows Vista les utilise dans tous les affichages, dans les boîtes de dialogue et pour tout type de fichier qui les fournit. D’autres applications peuvent également utiliser votre miniature. L’affichage des miniatures a également changé. à présent, un spectre continu de tailles sélectionnables par l’utilisateur est disponible au lieu des tailles discrètes, telles que les icônes et les miniatures fournies dans Windows XP.

> [!Note]  
> Vous pouvez entendre ces miniatures désignées par le terme « icônes dynamiques ».

 

les miniatures de résolution 32 bits et aussi volumineuses que les pixels 256x256 sont souvent utilisées dans l’interface utilisateur Windows Vista. Les propriétaires de format de fichier doivent être prêts à afficher leurs miniatures à cette taille. Ils doivent également fournir des images non statiques pour leurs miniatures qui reflètent le contenu d’un fichier particulier. Par exemple, la miniature d’un fichier texte doit afficher une version miniature du document, y compris son texte.

L’interface [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) a été introduite pour rendre une miniature plus facile et plus simple que dans le passé, lorsque [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) aurait été utilisé à la place. notez que le code existant qui utilise **IExtractImage** est toujours valide sous Windows Vista. Toutefois, **IExtractImage** n’est pas pris en charge dans le volet d' **informations** .

Cette rubrique traite des sujets suivants :

-   [Processus de miniatures](#thumbnail-processes)
-   [Cache de miniatures et dimensionnement](#thumbnail-cache-and-sizing)
-   [Superpositions de miniatures](#thumbnail-overlays)
-   [Ornements de miniatures](#thumbnail-adornments)
-   [Inscription de votre gestionnaire de miniatures](#registering-your-thumbnail-handler)
-   [Rubriques connexes](#related-topics)

## <a name="thumbnail-processes"></a>Processus de miniatures

Les gestionnaires, y compris les gestionnaires de miniatures, s’exécutent par défaut dans un processus distinct. Vous pouvez forcer le gestionnaire à s’exécuter in-process en passant une valeur **null** comme contexte de liaison dans un appel à [**IShellItem :: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) comme indiqué ici :


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



Vous pouvez également refuser l’exécution hors processus par défaut en définissant l’entrée DisableProcessIsolation dans le registre, comme indiqué dans cet exemple. L’identificateur de classe (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} est le CLSID pour les implémentations de [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Cache de miniatures et dimensionnement

quand une miniature est nécessaire, Windows vérifie d’abord le cache de miniatures pour l’image. L’extracteur de miniatures est appelé si l’image est introuvable dans le cache. Elle est également appelée lorsque l’heure de la dernière modification de l’image est ultérieure à celle de la copie dans le cache.

Les images miniatures de ce cache sont stockées dans un ensemble de tailles discrètes. Toutes les tailles sont exprimées en pixels.

-   32x32
-   96 x 96
-   256 x 256
-   1024 x 1024

> [!Note]  
> Ces valeurs sont sujettes à modification. Vous ne devez pas supposer que toute taille particulière sera toujours utilisée.

 

Si une image n’est pas carrée, vous ne devez pas la remplir vous-même. Windows est chargé de respecter les proportions d’origine et de remplir l’image à une taille carrée.

quand une image d’une taille particulière est demandée, sauf si une correspondance exacte est trouvée, Windows Vista récupère toujours la plus grande image suivante et la met à l’échelle jusqu’à la taille demandée. La taille d’une image n’est jamais augmentée, comme c’était le cas dans les versions précédentes de Windows.

Le tableau suivant donne quelques exemples de la relation entre la taille demandée et la taille disponible.



| Taille d’image maximale que vous fournissez | Taille demandée par l’extracteur | Vous fournissez                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156x120                        | 256 x 256                         | 156x120 (ne pas remplir, conserver les proportions) |
| 2048x1024                      | 256 x 256                         | 256 x 128 (ne pas remplir, conserver les proportions) |



 

Vous pouvez déclarer un point de coupure dans le cadre de l’entrée de l’ID de programme de l’application associée dans le registre. En dessous de cette taille, les miniatures ne sont pas utilisées.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

L’entrée ThumbnailCutoff est l’une de ces \_ valeurs de Reg DWORD.

| Valeur | Coupure | HighDPI sensible |
|-------|--------|-------------------|
| 0     | 32x32  | Oui               |
| 1     | 16x16  | Oui               |
| 2     | 48 x 48  | Oui               |
| 3     | 16x16  | Oui               |


La sensibilité en points par pouce (dpi) élevée signifie que les dimensions en pixels de la miniature s’ajustent automatiquement pour une résolution supérieure. Par exemple, une image 32x32 à 96 ppp serait une image 40 x 40 à 120 ppp.

Si l’entrée ThumbnailCutoff n’est pas spécifiée, la limite par défaut est 20x20 (non-respect de la dpi).

## <a name="thumbnail-overlays"></a>Superpositions de miniatures

Les superpositions de miniatures, une petite image affichée dans le coin inférieur droit de la miniature, donnent aux développeurs la possibilité d’appliquer une identification de marques à leurs miniatures. Les superpositions sont déclarées dans le registre dans le cadre de l’entrée de l’ID de programme de l’application associée, comme illustré ici :

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

L’entrée TypeOverlay contient une valeur de REG \_ SZ interprétée comme suit :

-   Si la valeur est une référence de ressource (un fichier **. ico** incorporé dans la dll) telle que `ISVComponent.dll,-155` , cette image est utilisée comme superposition pour les fichiers avec cette extension de nom de fichier. notez que dans cet exemple, **155** est l’ID de la ressource, et si la DLL n’est pas présente dans un chemin d’accès standard (par exemple, **C:/Windows/System32**), le chemin d’accès complet est requis au lieu de simplement le nom de la DLL.
-   Si la valeur est une chaîne vide, aucune superposition n’est appliquée à l’image.
-   Si la valeur n’est pas présente, l’icône par défaut de l’application associée est utilisée.

Les superpositions de vos miniatures doivent uniquement être fournies par le biais de ce mécanisme et appliquées par Windows. N’appliquez pas les superpositions vous-même.

## <a name="thumbnail-adornments"></a>Ornements de miniatures

Les ornements, tels que les ombres portées, sont appliqués aux miniatures en fonction du thème actuellement sélectionné par l’utilisateur. Les ornements sont fournis par Windows ; ne les créez pas vous-même. Windows pourriez modifier l’apparence d’ornements particuliers à tout moment. si vous vous êtes assuré, vous risquez de ne pas être synchronisé avec le système. Vos miniatures peuvent être plus ou moins récentes.

Les ornements potentiels sont déclarés dans le registre dans le cadre de l’entrée de l’ID de programme de l’application associée, comme illustré ici :

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

L’entrée de traitement contient une des valeurs de REG \_ DWORD suivantes :



| Valeur | Signification         |
|-------|-----------------|
| 0     | Aucun ornement    |
| 1     | Ombre portée     |
| 2     | Bordure photo    |
| 3     | Des fusées vidéo |


Une ombre portée est appliquée aux images par défaut.

## <a name="registering-your-thumbnail-handler"></a>Inscription de votre gestionnaire de miniatures

L’inscription d’un gestionnaire de miniatures est basée sur les associations de fichiers standard.

Le GUID de l’extension de Shell du gestionnaire de miniatures est `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Création de gestionnaires de miniatures](building-thumbnail-providers.md)
</dt> <dt>

[Instructions du gestionnaire de miniatures](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



