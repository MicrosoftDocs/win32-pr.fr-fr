---
title: Précautions relatives à la fonction de raccordement In-Context
description: Pour des raisons de performances, les développeurs clients inscrivent les fonctions de raccordement dans le contexte.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e319037cb1295725548b3361bf076b4b1f760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518284"
---
# <a name="in-context-hook-function-precautions"></a>Précautions relatives à la fonction de raccordement In-Context

Pour des raisons de performances, les développeurs clients inscrivent les fonctions de raccordement dans le contexte. Toutefois, étant donné que ces fonctions de raccordement sont mappées à l’espace d’adressage du serveur, les développeurs du client et du serveur doivent prendre des précautions pour garantir le bon déroulement du traitement des événements.

## <a name="precautions-for-client-developers"></a>Précautions pour les développeurs clients

Les développeurs clients doivent connaître les problèmes suivants :

-   Les fonctions de raccordement dans le contexte ne doivent pas utiliser beaucoup de temps processeur, car la fonction de raccordement doit retourner avant que l’application serveur continue.
-   Une fois qu’un événement est déclenché, il est possible que la fenêtre associée à un événement n’existe plus au moment de l’appel de la fonction de raccordement. Les clients doivent vérifier que la fenêtre associée à un événement existe toujours avant d’effectuer toute autre action liée à l’événement. Pour vous assurer qu’une fenêtre existe toujours, les clients utilisent la fonction Microsoft Win32 [**IsWindow**](/windows/desktop/api/winuser/nf-winuser-iswindow) .
-   Si la DLL dans laquelle la fonction de raccordement est définie est liée à une autre DLL, les développeurs clients doivent s’assurer que le système charge l’autre DLL. en cas de liaison implicite (à l’aide des fichiers. def et des importations), la DLL supplémentaire doit se trouver dans le répertoire Windows ou dans l’un des répertoires système tels que Windows \\ system, Windows \\ System32 ou Windows \\ SysWOW64. En cas de liaison explicite (à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)), le chemin d’accès complet au répertoire dans lequel réside la dll supplémentaire doit être spécifié dans l’appel à **LoadLibrary**.
-   Les fonctions de raccordement dans le contexte peuvent provoquer un dépassement de capacité de la pile lorsque la DLL qui contient la fonction de raccordement est chargée dans une application 16 bits. Ce problème se produit parce que les applications 16 bits utilisent une taille de pile fixe qui n’est pas suffisamment grande pour accueillir la chaîne d’appels de fonction système qui entraînent un appel à la fonction de raccordement.

## <a name="precautions-for-server-developers"></a>Précautions pour les développeurs de serveurs

Les développeurs de serveurs doivent savoir que les applications clientes peuvent inscrire des fonctions de raccordement dans le contexte. Lorsqu’un serveur appelle [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), il doit être préparé à gérer le [**WM \_ GETOBJECT**](wm-getobject.md) et d’autres méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="invalid-interface-pointers"></a>Pointeurs d’interface non valides

Lorsqu’un client appelle [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) dans une fonction de raccordement dans le contexte, le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) qui est retourné pointe directement vers le code dans l’espace d’adressage du serveur. Si le client appelle une propriété d’interface à l’aide de ce pointeur, la bibliothèque COM (Component Object Model) n’est pas impliquée dans le marshaling (empaquetage et envoi de paramètres d’interface au-delà des limites de processus) ou démarshaling (empaquetage des paramètres envoyés au-delà des limites de processus) et ne détecte pas si un objet est détruit

Si le client appelle une propriété d’interface sur un objet qui est détruit, le pointeur d’interface non valide provoque une erreur de protection générale dans l’espace d’adressage du serveur, sauf si le serveur détecte cette situation.

Pour vous protéger contre les pointeurs d’interface non valides, les serveurs [créent des objets proxy](creating-proxy-objects.md) qui encapsulent les objets accessibles et surveillent la durée de vie des objets accessibles. Par exemple, lorsqu’un client appelle une propriété [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour obtenir des informations sur un objet, le proxy vérifie si l’objet accessible est toujours disponible, et dans ce cas, transfère la demande du client à l’objet accessible. Si l’objet accessible est détruit, le proxy retourne une erreur au client.

 

 