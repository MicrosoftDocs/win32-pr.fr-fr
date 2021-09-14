---
title: ActiveX Contrôle les informations de Registre
description: ActiveX Contrôle les informations de Registre
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232800"
---
# <a name="activex-controls-registry-information"></a>ActiveX Contrôle les informations de Registre

Un certain nombre d’entrées de Registre et d’indicateurs sont utilisés. En outre, les contrôles peuvent prendre en charge des catégories de composants pour classer les fonctionnalités qu’ils fournissent.

Les clés de Registre liées aux contrôles sont signalées par un astérisque dans l’arborescence suivante :

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

L’entrée **DefaultIcon** est utilisée pour identifier une icône à afficher lorsque le contrôle est réduit à une icône. La fonction [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) est utilisée pour récupérer l’icône à partir du fichier .DLL ou .EXE spécifié.

L’entrée **ToolboxBitmap32** identifie le nom du module et l’identificateur de ressource pour une \* image bitmap 16 15 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils. la taille de l’icône de Windows standard est trop grande pour être utilisée à cet effet. Cette entrée prend en charge spécifiquement les conteneurs de contrôle qui ont un mode création dans lequel l’un sélectionne les contrôles et les place sur un formulaire en cours de conception. par exemple, dans Visual Basic, l’icône du contrôle s’affiche dans la boîte à outils Visual Basic en mode design.

L’entrée de **contrôle** marque un objet en tant que contrôle. Cette entrée est souvent utilisée par les conteneurs pour remplir des boîtes de dialogue. Le conteneur utilise cette sous-clé pour déterminer s’il faut inclure un objet dans une boîte de dialogue qui affiche des contrôles.

La sous-clé pouvant être **insérée** peut également être utilisée avec des contrôles, selon que l’objet peut agir uniquement comme un objet incorporé sur place sans fonctionnalités de contrôle spéciales. Les objets marqués avec l’option d' **insertion** s’affichent dans la boîte de dialogue Insérer un objet de leur conteneur. L’entrée pouvant être **insérée** signifie généralement que le contrôle a été testé avec des conteneurs sans contrôle.

Les sous-clés d' **insertion** et de **contrôle** sont facultatives. Un contrôle peut omettre la sous-clé pouvant être **insérée** s’il n’est pas conçu pour fonctionner avec des conteneurs plus anciens qui ne comprennent pas de contrôles. Un contrôle peut omettre la touche de **contrôle** s’il est conçu uniquement pour fonctionner avec un conteneur spécifique et ne souhaite donc pas être inséré dans d’autres conteneurs.

Les contrôles doivent avoir un verbe Properties, OLEIVERB \_ Properties, ainsi que tous les autres verbes qu’ils prennent en charge. Le verbe Properties, ainsi que le verbe standard OLEIVERB \_ Primary, fait en sorte que le contrôle affiche sa feuille de propriétés. Le verbe Properties est affiché en tant qu’élément Properties dans le menu du conteneur lorsque le contrôle est actif. De cette façon, le contrôle peut afficher sa propre page de propriétés, ce qui permet à l’utilisateur final de disposer de fonctionnalités utiles, même si le conteneur ne gère pas les contrôles.

Un contrôle définit la clé **MiscStatus** pour se décrire aux conteneurs potentiels. Les bits prennent les valeurs de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), et les contrôles ajoutent plusieurs valeurs à cette énumération. Pour plus d’informations, consultez les valeurs d’énumération **OLEMISC** . Le client peut obtenir ces informations en appelant [**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sans avoir à instancier le contrôle en premier.

Enfin, **version** décrit la version du contrôle qui doit correspondre à la version de la bibliothèque de types associée à ce contrôle.

De même, dans les informations de type pour un contrôle, le contrôle d’attribut marque une entrée de coclasse comme décrivant un contrôle.

 

 