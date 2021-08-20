---
title: IDirectWriterLock-implémentation de fichier composé
description: L’implémentation de fichier composé de IDirectWriterLock offre un moyen d’ouvrir un fichier composé en mode direct avec un seul Writer et plusieurs lecteurs.
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- IDirectWriterLock Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540806fd9c3907b53a50807a2ee60f5fdc0be9a3ad5ea753b52325533c5e9b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961879"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>IDirectWriterLock-implémentation de fichier composé

L’implémentation de fichier composé de [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) offre un moyen d’ouvrir un fichier composé en mode direct avec un seul Writer et plusieurs lecteurs.

Les fichiers composés peuvent être ouverts en mode direct à l’aide de l' \_ indicateur direct STGM. L’interface [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) définit l' \_ \| \_ \_ indicateur d’écriture Deny STGM share STGM ReadWrite \_ comme valide en mode direct sans nécessiter la surcharge d’une copie d’instantané.

Lorsqu’un fichier composé est ouvert en mode traité à l’aide de l' \_ indicateur STGM traité, vous pouvez également avoir plusieurs lecteurs et un seul enregistreur à l’aide de l' \_ indicateur d’écriture STGM ReadWrite \| STGM \_ share \_ Deny \_ . Toutefois, dans ce cas, une copie d’instantané du fichier est effectuée pour les lecteurs. Il existe souvent une surcharge d’une copie Scratch.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez l’implémentation fournie par le système de [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) lorsque vous ouvrez un stockage en mode direct (STGM \_ direct) avec les \_ indicateurs de partage STGM ReadWrite \| STGM \_ share \_ Deny \_ .

Pour obtenir un pointeur vers [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock), appelez **QueryInterface** sur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour obtenir l’objet de stockage racine pour le fichier composé.

Appelez [**IDirectWriterLock :: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) pour obtenir un accès en écriture exclusif à un fichier composé. Appelez [**IDirectWriterLock :: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) pour libérer l’accès en écriture exclusif.

[**IDirectWriterLock :: HaveWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) indique si le fichier est actuellement verrouillé.

## <a name="remarks"></a>Remarques

L’implémentation de fichier composé de la fonctionnalité à un seul Writer et à plusieurs lecteurs est basée sur le verrouillage de plage. L’enregistreur obtient un accès exclusif au stockage à écrire une fois que tous les lecteurs actuels ont fermé le stockage. Lorsque le writer est actif, les lecteurs suivants ne peuvent pas ouvrir le stockage. Le writer appelle [**IDirectWriterLock :: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) pour obtenir un accès en écriture exclusif. Le writer doit ensuite appeler [**IDirectWriterLock :: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) pour libérer le stockage.

L’appel à [**IDirectWriterLock :: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) est requis avant l’écriture dans ce mode à lecteur unique et à Writer multiple. Les tentatives d’écriture dans le fichier sans appeler **IDirectWriterLock :: WaitForWriteAccess** génèrent d’abord STG \_ E \_ ACCESSDENIED. Cette erreur est retournée même si le writer a ouvert le fichier initialement et qu’aucun lecteur n’est actuellement ouvert dans ce fichier.

## <a name="marshaling-considerations"></a>Considérations relatives au marshaling

Le marshaling personnalisé est généralement utilisé lorsqu’un fichier composé est marshalé vers un autre processus sur le même ordinateur. Lors du marshaling des stockages, les droits d’accès ne sont pas pris en compte et le pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) est passé au nouveau processus avec les mêmes modes d’accès et droits que le processus de marshaling d’origine. Pour plus d’informations sur les modes d’accès, consultez [**constantes STGM**](stgm-constants.md). Pendant le marshaling, aucun verrou n’est pris ou vérifié pour garantir un accès en écriture exclusif. Dans ce cas, il n’y a pas d’application de la stratégie de rédacteur unique pour les fichiers composés ouverts dans le mode à un seul Writer et à lecteur multiple. Au lieu de cela, la mise en œuvre est gérée en interne par l’implémentation du fichier composé.

Étant donné que le pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) est passé à un autre processus pendant le marshaling, deux processus peuvent accéder simultanément au même fichier composé. Même si un appelant peut avoir obtenu un accès en écriture exclusif au stockage en appelant [**IDirectWriterLock :: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), la version marshalée peut également avoir un accès simultané. Les versions marshalées ne sont pas obligées de se fermer lorsque le seul rédacteur accède au fichier. Dans ce cas, l’implémentation de fichier composé synchronise les écritures en interne.

Si un writer unique obtient l’accès exclusif en appelant, [**IDirectWriterLock :: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), le stockage marshalé dispose également d’un accès en écriture et n’a pas besoin d’appeler **IDirectWriterLock :: WaitForWriteAccess**. Les deux processus ont un accès en écriture et la synchronisation est contrôlée par l’implémentation de fichier composé interne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




