---
title: Vue d’ensemble de DWriteCore
description: DWriteCore est l’implémentation de réunion de projet de DirectWrite.
keywords:
- Le noyau de DirectWrite
- DWriteCore
ms.topic: article
ms.date: 04/21/2021
ms.openlocfilehash: 27a34656ce28a65267bd098974b4df9003a80e17
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881838"
---
# <a name="dwritecore-overview"></a>Vue d’ensemble de DWriteCore

DWriteCore est l’implémentation de [réunion de projet](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md) (DirectWrite est l’API DirectX pour le rendu de texte de haute qualité, les polices de plan indépendantes de la résolution et la prise en charge complète du texte et de la disposition Unicode). DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.

Cette rubrique d’introduction décrit ce que DWriteCore est, et montre comment l’installer dans votre environnement de développement et votre programme avec lui.

## <a name="the-value-proposition-of-dwritecore"></a>La proposition de valeur de DWriteCore

[DirectWrite](./direct-write-portal.md) prend en charge un large éventail de fonctionnalités qui en font l’outil de rendu des polices de choix sur Windows pour la plupart des applications &mdash; , que ce soit via des appels directs ou via [Direct2D](../direct2d/direct2d-portal.md). DirectWrite comprend un système de disposition de texte indépendant du périphérique, un rendu de texte [Microsoft ClearType](/typography/cleartype/) de qualité supérieure, du texte accéléré par le matériel, du texte à plusieurs formats, des fonctionnalités avancées de typographie [® OpenType](/typography/opentype/) , une prise en charge de langage large et une disposition et un rendu compatibles [GDI](../gdi/windows-gdi.md). DirectWrite est disponible depuis Windows Vista SP2 et a évolué au fil des années pour inclure des fonctionnalités plus avancées, telles que des polices variables, qui permettent aux développeurs d’appliquer des styles, des pondérations et d’autres attributs à une police avec une seule ressource de police.

En raison de la longue durée de validité de DirectWrite, toutefois, les avancées en matière de développement ont tendance à conserver des versions antérieures de Windows. En outre, l’état de DirectWrite en tant que technologie de rendu de texte premier est limité uniquement à Windows, ce qui laisse les applications multiplateformes écrire leur propre pile de rendu de texte, ou s’appuyer sur des solutions tierces.

DWriteCore résout les problèmes fondamentaux de la fonctionnalité de la version orpheline et de la compatibilité multiplateforme en supprimant la bibliothèque du système et en ciblant tous les points de terminaison possibles pris en charge. À cette fin, nous avons intégré DWriteCore dans le projet de réunion avec une API publique qui est prise en charge sur tous les points de terminaison Windows jusqu’à Windows 8, et qui ouvre la porte pour que vous l’utilisiez sur plusieurs plateformes.

La valeur principale que DWriteCore vous offre, en tant que développeur, dans le projet de réunion, est qu’elle permet d’accéder à toutes les fonctionnalités de DirectWrite actuelles jusqu’à Windows 8. Toutes les fonctionnalités de DWriteCore fonctionneront de la même façon sur toutes les versions de niveau supérieur. en d’autres termes, toutes les fonctionnalités actuelles fonctionnent sur Windows 8, 8,1 et toutes les versions de Windows 10, sans aucune disparité quant aux fonctionnalités qui peuvent fonctionner sur les versions de.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Application de démonstration DWriteCore &mdash; DWriteCoreGallery

DWriteCore est démontré par le biais de l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que vous pouvez maintenant télécharger et étudier.

## <a name="get-started-with-dwritecore"></a>Prise en main de DWriteCore

DWriteCore fait partie de la [réunion de projet 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0). Cette section décrit comment configurer votre environnement de développement pour la programmation avec DWriteCore.

### <a name="install-the-project-reunion-05-vsix"></a>Installer le projet de réunion 0,5 VSIX

Dans Visual Studio, cliquez sur **Extensions**  >  **gérer les extensions**, recherchez *projet de réunion* et téléchargez l’extension de réunion de projet. Fermez et rouvrez Visual Studio, puis suivez les invites pour installer l’extension.

Pour plus d’informations, consultez [projet REUNION 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)et [créer des applications Windows pour ordinateur de bureau avec la réunion de projet 0,5](/windows/apps/project-reunion/#set-up-your-development-environment).

### <a name="create-a-new-project"></a>Créer un projet

Dans Visual Studio, créez un projet à partir du modèle de projet **application vide, empaqueté (WinUI 3 dans le bureau)** . Vous pouvez trouver ce modèle de projet en choisissant langue : *C++*; plateforme : *projet REUNION*; type de projet : *Bureau*.

Pour plus d’informations, consultez [modèles de projet pour WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Installer le package NuGet Microsoft. ProjectReunion. DWrite

Dans Visual Studio, cliquez sur **projet** \> **gérer les packages NuGet...** \> **Parcourir**, tapez ou collez **Microsoft. ProjectReunion. DWrite** dans la zone de recherche, sélectionnez l’élément dans les résultats de la recherche, puis cliquez sur **installer** pour installer le package pour ce projet.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Vous pouvez également commencer par l’exemple d’application DWriteCoreGallery

Vous pouvez également programmer avec DWriteCore en commençant par l’exemple de projet d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , et baser votre développement sur ce projet. Vous pouvez alors librement supprimer le code source (ou les fichiers) existant de cet exemple de projet et ajouter un nouveau code source (ou des fichiers) au projet.

### <a name="use-dwritecore-in-your-project"></a>Utiliser DWriteCore dans votre projet

Pour plus d’informations sur la programmation avec DWriteCore, consultez la section [programmation avec DWriteCore](#programming-with-dwritecore) plus loin dans cette rubrique.

## <a name="the-release-phases-of-dwritecore"></a>Phases de publication de DWriteCore

Le portage de DirectWrite vers DWriteCore est un projet suffisamment volumineux pour s’étendre sur plusieurs cycles de publication Windows. Ce projet est divisé en plusieurs phases, chacune correspondant à un segment de fonctionnalités fournies dans une version.

### <a name="features-in-the-current-release-of-dwritecore"></a>Fonctionnalités de la version actuelle de DWriteCore

La version de DWriteCore actuellement disponible contient les outils de base que vous, en tant que développeur, devez utiliser DWriteCore, y compris les fonctionnalités suivantes.

- Énumération des polices.
- API de police.
- Shaping.
- API de rendu de bas niveau. Cela est partiel au niveau de la phase actuelle &mdash; DWriteCore n’interagit pas avec [Direct2D](../direct2d/direct2d-portal.md), mais vous pouvez utiliser [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) et [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Fonctionnalités de base de la disposition du texte.
- API de rendu de texte.
- Cible de rendu bitmap.
- Polices de couleur.
- Optimisations diverses (nettoyage du cache des polices, chargeur de police en mémoire, etc.).

La fonctionnalité de bannière à ce niveau est polices de couleurs. Les polices de couleur vous permettent de restituer vos polices avec des fonctionnalités de couleur plus sophistiquées que des couleurs simples simples. Par exemple, les polices de couleur permettent de rendre les polices d’Emoji et d’icône de barre d’outils (la dernière qui est utilisée par Office, par exemple). Les polices de couleur ont été introduites pour la première fois dans Windows 8.1, mais la fonctionnalité a été largement développée sur Windows 10, version 1607 (mise à jour anniversaire).

Le travail au nettoyage du cache de polices et le chargeur de police en mémoire permettent un chargement plus rapide des polices et des améliorations de la mémoire.

Grâce à ces fonctionnalités, vous pouvez commencer immédiatement à exploiter certaines fonctionnalités de base modernes de DirectWrite &mdash; , telles que les polices variables &mdash; de niveau inférieure vers Windows 8. Cette itération de la bibliothèque peut également être consommée sur [Android](https://www.android.com/)et **Linux**. Les polices variables sont l’une des fonctionnalités les plus importantes pour les clients de DirectWrite. ils ont été introduits dans Windows 10, version 1709 (automne Creators Update). par conséquent, l’accès aux versions précédentes est une aubaine importante pour vous en tant que développeur.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Notre invitation en tant que développeur DirectWrite

DWriteCore, ainsi que d’autres composants de réunion de projet, seront développés avec les commentaires des développeurs. Nous vous invitons à commencer à explorer DWriteCore et à fournir des informations ou des demandes dans le développement de fonctionnalités sur notre [référentiel GitHub de réunion de projet](https://github.com/microsoft/ProjectReunion/).

## <a name="programming-with-dwritecore"></a>Programmation avec DWriteCore

Comme avec [DirectWrite](./direct-write-portal.md), vous programmez avec DWriteCore via son API com-Light, via l’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

Pour utiliser DWriteCore, il est nécessaire d’inclure le `dwrite_core.h` fichier d’en-tête.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

Le `dwrite_core.h` fichier d’en-tête définit d’abord le jeton *DWRITE_CORE*, puis il comprend `dwrite_3.h` . Le jeton *DWRITE_CORE* est important, car il dirige tous les en-têtes inclus ultérieurement pour rendre toutes les API DirectWrite disponibles. Une fois votre projet inclus `dwrite_core.h` , vous pouvez continuer à écrire du code, le générer et l’exécuter.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>API nouvelles ou différentes pour DWriteCore

La surface de l’API DWriteCore est la plus similaire à celle de [DirectWrite](/windows/win32/api/_directwrite/). Mais il existe un petit nombre de nouvelles API qui se trouvent uniquement dans DWriteCore à l’heure actuelle.

#### <a name="create-a-restricted-factory-object"></a>Créer un objet de fabrique restreint

L’énumération [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) a une nouvelle constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indiquant une fabrique restreinte. Une fabrique restreinte est plus verrouillée qu’une fabrique isolée. Il n’interagit d’aucune manière avec un cache de polices interprocessus ou persistant. En outre, la collection de polices système retournée par cette fabrique comprend uniquement des polices bien connues. Voici comment vous pouvez utiliser **DWRITE_FACTORY_TYPE_ISOLATED2** pour créer un objet de fabrique restreint lorsque vous appelez la fonction Free [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) .

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Si vous transmettez **DWRITE_FACTORY_TYPE_ISOLATED2** à une version antérieure de DirectWrite qui ne la prend pas en charge, **DWriteCreateFactory** retourne **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Dessin de glyphes dans une bitmap de mémoire système

DirectWrite a une interface cible de rendu bitmap qui prend en charge le rendu des glyphes à une image bitmap dans la mémoire système. Toutefois, actuellement, la seule façon d’accéder aux données de pixels sous-jacentes est de traverser GDI, et l’API n’est donc pas utilisable sur plusieurs plateformes. Cela est facilement résolu en ajoutant une méthode pour récupérer les données de pixels.

DWriteCore introduit l’interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) et sa méthode [**IDWriteBitmapRenderTarget2 :: GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Cette méthode prend un paramètre de type (pointeur vers) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), qui est un nouveau struct.

Votre application crée une cible de rendu bitmap en appelant [IDWriteGdiInterop :: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). Sur Windows, une cible de rendu bitmap encapsule un DC de mémoire GDI avec une bitmap indépendante du périphérique (DIB) GDI sélectionnée. [IDWriteBitmapRenderTarget ::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) affiche les glyphes dans le dib. DirectWrite rend les glyphes eux-mêmes sans passer par GDI. Votre application peut ensuite obtenir le **HDC** à partir de la cible de rendu bitmap et utiliser [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) pour copier les pixels dans un **HDC** de fenêtre.

Sur les plateformes non-Windows, votre application peut toujours créer une cible de rendu bitmap, mais elle encapsule simplement un tableau de mémoire système sans **HDC** ni dib. Sans **HDC**, votre application doit disposer d’une autre méthode pour obtenir les pixels de la bitmap, afin qu’elle puisse les copier ou les utiliser dans d’autres cas. Même sur Windows, il est parfois utile d’acquérir les données de pixels réelles, et nous allons montrer la façon actuelle de le faire dans l’exemple de code ci-dessous.

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Autres différences d’API entre DWriteCore et DirectWrite

Il existe quelques API qui sont soit des stubs, soit elles se comportent différemment sur des plateformes non-Windows. Par exemple, [IDWriteGdiInterop :: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retourne **E_NOTIMPL** sur les plateformes non-Windows, car il n’y a pas d’autre chose qu’un **HDC** sans [GDI](../gdi/windows-gdi.md).

Enfin, il existe certaines API Windows qui sont généralement utilisées avec DirectWrite (Direct2D étant un exemple notable). Toutefois, à l’heure actuelle, Direct2D et DWriteCore n’interagissent pas. Par exemple, si vous créez un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de DWriteCore et que vous le transmettez à [**D2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), l’appel échoue.
