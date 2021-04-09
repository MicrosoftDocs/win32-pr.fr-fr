---
title: Descripteurs implicites et explicites
description: Pour déclarer un handle de sérialisation, utilisez le handle de type de handle primitif \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842614"
---
# <a name="implicit-vs-explicit-handles"></a>Descripteurs implicites et explicites

Pour déclarer un handle de sérialisation, utilisez le handle de type de handle primitif [**\_ t**](/windows/desktop/Midl/handle-t). Les handles de sérialisation peuvent être explicites ou implicites. Spécifiez des handles implicites dans le CCP de votre application à l’aide de l’attribut de **\[ \_ handle \] implicite** . Le compilateur MIDL génère une variable de handle de sérialisation globale. Les procédures de sérialisation avec un handle implicite utilisent cette variable globale pour accéder à un contexte de sérialisation valide.

Lors de l’utilisation de l’encodage de type, les routines générées prenant en charge la sérialisation d’un type particulier utilisent le handle implicite global pour accéder au contexte de sérialisation. Notez que les routines distantes peuvent avoir besoin d’utiliser le handle implicite comme handle de liaison. Assurez-vous que le handle implicite est défini sur un handle de sérialisation valide avant d’effectuer un appel de sérialisation.

Un handle explicite est spécifié en tant que paramètre du prototype de procédure de sérialisation dans le fichier IDL, ou il peut également être spécifié à l’aide de l’attribut **\[ \_ handle \] explicite** dans le CCP. Le paramètre de handle explicite est utilisé pour établir le contexte de sérialisation approprié pour la procédure. Pour établir le contexte correct dans le cas de la sérialisation de type, le compilateur génère les routines de prise en charge qui utilisent le paramètre [**\_ t Handle**](/windows/desktop/Midl/handle-t) explicite comme handle de sérialisation. Vous devez fournir un handle de sérialisation valide lors de l’appel d’une procédure de sérialisation ou d’une routine de prise en charge de type de sérialisation.

 

 