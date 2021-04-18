---
description: Commencez à apprendre les principes fondamentaux de la création d’applications de bureau performantes dans cette section.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Bien démarrer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513153"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Bien démarrer avec les applications de bureau Windows qui utilisent l’API Win32

L’API Win32 (également appelée API Windows) est la plateforme d’origine pour les applications Windows C/C++ natives qui nécessitent un accès direct à Windows et au matériel. Il fournit une expérience de développement de premier ordre sans dépendre d’un environnement d’exécution managé tel que .NET et WinRT (pour les applications UWP pour Windows 10). L’API Win32 est donc la plateforme de choix pour les applications qui ont besoin de performances au plus haut niveau et d’un accès direct au matériel système.

> [!NOTE]
> Cette documentation explique comment créer des applications Windows bureautiques avec l’API Win32. L’API Win32 est l’une des différentes plateformes d’application que vous pouvez utiliser pour créer des applications Windows bureautiques. Pour plus d’informations sur les autres plateformes d’application, consultez [choisir votre plateforme](/windows/apps/desktop/choose-your-platform).

## <a name="get-set-up"></a>Se préparer

Suivez ces instructions et commencez à créer des applications de bureau pour Windows 10 qui utilisent l’API Win32.

1. Téléchargez ou mettez à jour Visual Studio 2019. Si vous ne possédez pas Visual Studio 2019, vous pouvez installer gratuitement Microsoft Visual Studio Community 2019. Quand vous installez Visual Studio, veillez à sélectionner l’option **développement bureautique en C++** . Pour obtenir des liens de téléchargement, consultez notre page de [téléchargements](https://developer.microsoft.com/windows/downloads) .

    > [!NOTE]
    > Quand vous installez Visual Studio, vous pouvez éventuellement sélectionner les options de développement et de développement du **Bureau .net** et de **plateforme Windows universelle** pour accéder à d’autres types de projets et plateformes d’application pour la création d’applications Windows bureautiques.

2. Si vous souhaitez créer votre application de bureau dans un [package MSIX](/windows/msix/desktop/desktop-to-uwp-root) et tester ou déboguer l’application empaquetée sur votre ordinateur de développement, vous devez [activer le mode développeur sur votre ordinateur](/windows/uwp/get-started/enable-your-device-for-development).

> [!NOTE]
> Pour les scripts que vous pouvez utiliser pour configurer votre ordinateur de développement et installer d’autres fonctionnalités ou packages, consultez [ce projet GitHub](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Découvrez comment créer des applications de bureau à l’aide de l’API Win32

Si vous n’êtes pas en train de créer des applications de bureau à l’aide de l’API Win32, les didacticiels et les articles suivants vous aideront à démarrer.

| Rubrique        | Description      |
|---------------|-----------------|
| [Créer votre première application C++ Win32](LearnWin32/learn-to-program-for-windows.md)    | Ce didacticiel vous apprend à écrire un programme Windows en C++ à l’aide des API Win32 et COM.  |
| [Créer votre première application à l’aide de DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Ce didacticiel de base vous aidera à démarrer le développement d’applications DirectX.            |
| [Guide de programmation pour Windows 64 bits](WinProg64/programming-guide-for-64-bit-windows.md)    | Décrit la programmation pour les versions 64 bits du système d’exploitation Windows. |
| [Utilisation des en-têtes Windows](WinProg/using-the-windows-headers.md)     | Fournit une vue d’ensemble de certaines des conventions utilisées dans les fichiers d’en-tête Windows. |

Vous pouvez également parcourir les [exemples d’applications de bureau](https://github.com/Microsoft/Windows-classic-samples).

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Moderniser vos applications de bureau pour Windows 10

Si vous disposez déjà d’une application de bureau Win32, vous pouvez utiliser de nombreuses fonctionnalités de la plateforme Windows universelle (UWP) pour offrir la meilleure expérience possible sur Windows 10. Par exemple, à compter de la version 1903 de Windows 10, vous pouvez héberger des contrôles XAML UWP dans votre application Desktop Win32 à l’aide d’une fonctionnalité appelée îlots XAML.

La plupart de ces fonctionnalités UWP sont disponibles sous forme de composants modulaires que vous pouvez adopter dans votre application de bureau à votre rythme sans avoir à réécrire l’intégralité de votre application. Vous pouvez améliorer votre application de bureau existante en choisissant les parties de Windows 10 et UWP à adopter.

Pour plus d’informations, consultez [Moderniser vos applications de bureau](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Si vous le souhaitez, vous pouvez configurer votre ordinateur de développement pour utiliser [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/). C++/WinRT est une projection de langage C++ 17 moderne, entièrement standard, qui vous permet de consommer facilement des API Windows Runtime API Windows Runtime (WinRT) à partir de votre application de bureau C++ Win32. C++/WinRT est implémenté en tant que bibliothèque basée sur un fichier d’en-tête.

Pour configurer votre projet pour C++/WinRT :

* Pour de nouveaux projets, vous pouvez installer l’[Extension Visual Studio (VSIX) C++/WinRT](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) et utiliser l’un des modèles de projet C++/WinRT inclus dans cette extension.
* Pour les projets d’application de bureau Windows existants, vous pouvez installer le package NuGet [Microsoft. Windows. CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) dans le projet.

Pour plus d’informations sur ces options, consultez [cet article](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Nouveautés des API Win32 dans Windows 10

Pour en savoir plus sur les nouvelles API Win32 qui ont été introduites dans Windows 10, consultez [Nouveautés](whats-new.md).

## <a name="get-started-with-win32-features-and-technologies"></a>Prise en main des fonctionnalités et technologies Win32

Les API Win32 existent pour de nombreuses fonctionnalités et technologies dans Windows 10, y compris l’interface utilisateur principale et les API de fenêtrage, l’audio et les graphiques, et la mise en réseau. Pour obtenir des instructions et des exemples de code sur l’utilisation de ces API, [consultez notre index sur les fonctionnalités et technologies](desktop-app-technologies.md).

## <a name="related-topics"></a>Rubriques connexes

* [Développer des applications de bureau](/windows/apps/desktop)
* [Informations de référence sur l’API Windows](/windows/desktop/api/)
* [Index des API Windows](/windows/desktop/apiindex/api-index-portal)
* [Informations de référence sur Windows Runtime C++](/windows/desktop/winrt/reference)
