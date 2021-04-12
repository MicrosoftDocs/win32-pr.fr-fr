---
description: Les ensembles d’API sont des groupes fonctionnels d’API Win32 dans le système d’exploitation principal. Ils fournissent une séparation architecturale à partir de la DLL hôte dans laquelle une API Win32 donnée est définie et du groupe fonctionnel auquel appartient l’API.
title: Ensembles d’API Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104463979"
---
# <a name="windows-api-sets"></a>Ensembles d’API Windows

Toutes les versions de Windows 10 partagent une base commune de composants du système d’exploitation appelée *système d’exploitation* de base (dans certains contextes, cette base commune est également appelée *OneCore*). Dans les composants du système d’exploitation de base, les API Win32 sont organisées en groupes fonctionnels appelés *ensembles d’API*.

L’objectif d’un ensemble d’API est de fournir une séparation architecturale à partir de la DLL hôte dans laquelle une API Win32 donnée est implémentée et le contrat fonctionnel auquel appartient l’API. Le découplage que les ensembles d’API offrent entre les implémentations et les contrats offre de nombreux avantages en matière d’ingénierie pour les développeurs. En particulier, l’utilisation d’ensembles d’API dans votre code peut améliorer la compatibilité avec tous les appareils Windows 10.

Les ensembles d’API concernent spécifiquement les scénarios suivants :

- Bien que la totalité de l’API Win32 soit prise en charge sur les PC, seul un sous-ensemble de l’API Win32 est disponible sur d’autres appareils Windows 10 tels que HoloLens, Xbox et d’autres appareils exécutant Windows 10x. Le nom de l’ensemble d’API fournit un mécanisme de requête pour détecter correctement si une API est disponible sur un appareil donné.

- Certaines implémentations de l’API Win32 existent dans des dll avec des noms différents sur différents appareils Windows 10. Le fait d’utiliser des noms d’ensemble d’API au lieu de noms de DLL lors de la détection des API de disponibilité et de chargement différé fournit un itinéraire correct à l’implémentation, quel que soit l’endroit où l’API est implémentée.

Pour plus d’informations, consultez [API Set Loader Operation](api-set-loader-operation.md) et [Detect API Set Availability](detect-api-set-availability.md).

## <a name="linking-to-umbrella-libraries"></a>Liaison à des bibliothèques de parapluie

Pour faciliter la restriction de votre code aux API Win32 qui sont prises en charge dans le système d’exploitation de base, nous fournissons une série de *bibliothèques de parapluie*. Par exemple, une bibliothèque de parapluie nommée OneCore. lib fournit les exportations pour le sous-ensemble d’API Win32 qui sont communes à tous les appareils Windows 10.

Les API d’une bibliothèque de parapluie peuvent être implémentées dans une plage de modules. La bibliothèque parapluie résume ces détails en dehors de vous, ce qui rend votre code plus portable sur les versions et les appareils Windows 10. Au lieu de créer des liens vers des bibliothèques telles que kernel32. lib et advapi32. lib, il vous suffit de lier votre application de bureau ou pilote à la bibliothèque parapluie qui contient l’ensemble des API de système d’exploitation principales qui vous intéressent.

Pour plus d’informations, consultez [bibliothèques de parapluie Windows](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>Noms de contrat de l’ensemble d’API

Les ensembles d’API sont identifiés par un nom de contrat fort qui respecte les conventions standard reconnues par le chargeur de bibliothèque. 

- Le nom doit commencer par l' **API de** chaîne ou **ext-**. 
    - Les noms qui commencent par **API-** représentent des API qui sont garanties d’exister sur toutes les versions de Windows 10.
    - Les noms qui commencent par **ext-** représentent des API qui n’existent peut-être pas dans toutes les versions de Windows 10.
- Le nom doit se terminer par la **séquence \<n\> - \<n\> - \<n\> l**, où **n** est constitué de chiffres décimaux.
- Le corps du nom peut être des caractères alphanumériques ou des tirets ( **-** ).
- Le nom ne respecte pas la casse.

Voici quelques exemples de noms de contrat d’ensemble d’API :

- **API-MS-Win-Core-UMS-L1-1-0**
- **ext-MS-Win-com-ole32-L1-1-5**
- **ext-MS-Win-Ntuser-Window-L1-1-0**
- **ext-MS-Win-Ntuser-Window-L1-1-1**

Vous pouvez utiliser un nom d’ensemble d’API dans le contexte d’une opération de chargement comme [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [P/Invoke](/dotnet/standard/native-interop/pinvoke) à la place d’un nom de module dll pour garantir un itinéraire correct vers l’implémentation, quel que soit l’endroit où l’API est réellement implémentée sur l’appareil actuel. Toutefois, lorsque vous effectuez cette opération, vous devez ajouter le **fichier String. dll** à la fin du nom du contrat. Il s’agit d’une condition requise du chargeur pour fonctionner correctement et n’est pas considérée comme faisant partie du nom de contrat. Bien que les noms de contrats apparaissent comme les noms de DLL dans ce contexte, ils sont fondamentalement différents des noms de module de DLL et ne font pas directement référence à un fichier sur le disque.

À l’exception de l’ajout de String **. dll** dans les opérations du chargeur, les noms de contrat de l’ensemble d’API doivent être considérés comme un identificateur immuable qui correspond à une version de contrat spécifique.

## <a name="identifying-api-sets-for-win32-apis"></a>Identification des ensembles d’API pour les API Win32

Pour déterminer si une API Win32 particulière appartient à un ensemble d’API, consultez le tableau des exigences dans la documentation de référence de l’API. Si l’API appartient à un ensemble d’API, le tableau des exigences de l’article répertorie le nom de l’ensemble d’API et la version de Windows dans laquelle l’API a été introduite pour la première fois dans l’ensemble d’API. Pour obtenir des exemples d’API appartenant à un ensemble d’API, consultez les articles suivants :

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>Dans cette section

* [Opération du chargeur de l’ensemble d’API](api-set-loader-operation.md)
* [Détecter la disponibilité des ensembles d’API](detect-api-set-availability.md)
* [Bibliothèques parapluies Windows](windows-umbrella-libraries.md)