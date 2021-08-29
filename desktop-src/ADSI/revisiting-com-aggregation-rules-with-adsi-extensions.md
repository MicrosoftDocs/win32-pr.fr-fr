---
title: Réexaminer les règles d’agrégation COM avec les extensions ADSI
description: Voici un bref aperçu de l’agrégation COM et des règles d’extension ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- ADSI d’extensions, règles d’agrégation COM
- ADSI Aggregation COM
- Réexaminer les règles d’agrégation COM avec les extensions ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e3f5500102a77b8dbc69a66cfb864b1fdb6a2cd842adb7cd2042429dc838c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770779"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Réexaminer les règles d’agrégation COM avec les extensions ADSI

Voici un bref aperçu de l’agrégation COM et des règles d’extension ADSI.

-   La méthode **CreateInstance** retourne un pointeur vers une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , comme suit, qui ne délègue aucun appel de fonction à l’agrégation.

    La méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) retourne des pointeurs vers les interfaces qu’il prend en charge, ainsi que des erreurs pour les interfaces qu’il ne prend pas en charge.

    La méthode [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrémente le décompte de références sur l’objet d’extension agrégé lui-même.

    La méthode [**IUnkown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) décrémente le décompte de références sur l’objet d’extension agrégé lui-même et se détruit lorsque le nombre de références est égal à 0.

-   L’objet d’extension doit stocker le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’agrégateur, tel que m \_ pOuterUnknown, pendant l’implémentation de la méthode **CreateInstance** .
-   Toutes les interfaces prises en charge par l’objet d’extension, y compris [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), doivent hériter de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), qui délègue tous les appels de fonction à l’agrégateur.
    -   [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) appelle « m \_ POuterUnknown->QueryInterface »
    -   [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) appelle « m \_ POuterUnknown->AddRef »
    -   [**IUnkown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) appelle « m \_ POuterUnknown->Release »

Les rédacteurs d’extensions peuvent choisir n’importe quelle implémentation interne qu’ils préfèrent, à condition qu’ils respectent les règles d’agrégation COM standard. N’oubliez pas qu’un objet d’extension ne doit pas nécessairement fonctionner comme un objet autonome. Les extensions sont conçues pour fonctionner en tant qu’agrégats. Toutefois, une extension peut être écrite pour fonctionner à la fois comme un objet autonome et comme un agrégat.

En plus de la prise en charge de l’agrégation COM standard, un objet d’extension peut prendre en charge [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour des fonctionnalités plus avancées. Si la liaison tardive est prise en charge, l’extension doit :

-   Déléguez les fonctions pour [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) à l’agrégateur.
-   Implémentez l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) dans [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 