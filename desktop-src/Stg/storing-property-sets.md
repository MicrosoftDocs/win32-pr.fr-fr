---
title: Stockage des jeux de propriétés
description: Les applications peuvent exposer certaines données d’état de leurs documents afin que d’autres applications puissent les localiser et les lire.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- stockage des jeux de propriétés Stockage structurés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beae3d03889415fd920cb34d065c0ffd33e813b170d45dd73ae7c4d548f9296d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661779"
---
# <a name="storing-property-sets"></a>Stockage des jeux de propriétés

Les applications peuvent exposer certaines données d’état de leurs documents afin que d’autres applications puissent les localiser et les lire. Certains exemples sont un jeu de propriétés qui décrit l’auteur, le titre et les mots clés d’un document créé avec un traitement de texte, ou la liste des polices utilisées dans un document. Cette fonctionnalité n’est pas limitée aux documents ; Il peut également être utilisé sur des objets incorporés. En règle générale, l’accès aux jeux de propriétés doit être via les interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , mais cette section décrit la méthode recommandée précédemment.

> [!Note]  
> Si vous stockez un jeu de propriétés qui est interne à votre application, vous pouvez ne pas vouloir suivre les indications ci-dessous. Pour exposer votre propriété à d’autres applications, suivez ces instructions.

 

**Pour stocker un jeu de propriétés dans un fichier composé**

1.  Créez une instance [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) dans le même niveau de la structure de stockage que ses flux de données. Suivez le nom de votre instance **IStorage** ou **IStream** avec « \\ 005 ». Les noms de flux et de stockage qui commencent par 0x05 sont réservés aux jeux de propriétés communes qui peuvent être partagés entre les applications. En outre, les flux commençant par cette valeur sont limités à 256 Ko. les noms peuvent être sélectionnés à partir de noms et de formats publiés, ou en affectant la propriété définir un FMTID et en dérivant le nom du FMTID conformément aux conventions décrites dans [Stockage les conventions d’affectation](storage-object-naming-conventions.md)des noms d’objets.
2.  Un jeu de propriétés peut être stocké dans une instance [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) unique ou dans une instance [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) contenant plusieurs flux et stockages. Dans le cas d’une instance de **IStorage** , le flux de contenu nommé contents est le flux principal contenant des valeurs de propriété, où certaines valeurs peuvent être des noms d’autres flux ou instances de stockage dans le stockage pour ce jeu de propriétés.
3.  Spécifiez le CLSID de la classe d’objet qui peut afficher ou fournir un accès par programme aux valeurs de propriété. S’il n’existe aucune classe de ce type, le CLSID doit être défini sur l’identificateur de format du jeu de propriétés. Pour un jeu de propriétés qui utilise une instance de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , définissez le CLSID de l’instance de **IStorage** de manière à ce qu’il soit identique à celui stocké dans le flux de contenu ou à **CLSID \_ null**; valeur dans une instance **IStorage** nouvellement créée.
4.  Vous avez la possibilité de spécifier des noms affichables qui constituent le contenu du dictionnaire.

Certaines applications peuvent lire uniquement des implémentations de jeux de propriétés stockées en tant qu’instances [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) . Les applications doivent être écrites pour s’attendre à ce qu’un jeu de propriétés puisse être stocké dans une instance [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou **IStream** , à moins que la définition du jeu de propriétés indique le contraire. Par exemple, la définition du jeu de propriétés informations de synthèse indique qu’elle peut uniquement être stockée dans une instance **IStream** nommée. Dans les cas où vous recherchez un jeu de propriétés et que vous ne savez pas s’il s’agit d’un stockage ou d’un flux, recherchez d’abord une instance **IStream** avec votre nom de jeu de propriétés. En cas d’échec, recherchez une instance **IStorage** .

Pour mieux comprendre le stockage des jeux de propriétés dans une implémentation [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , supposez qu’il existe une classe d’applications qui modifient les informations sur les animaux. Tout d’abord, un CLSID (CLSID \_ AnimalApp) est défini pour cet ensemble d’applications. ils peuvent donc indiquer qu’ils comprennent les jeux de propriétés qui contiennent des informations animales (**fmtid \_ AnimalInfo**) et d’autres qui contiennent des informations médicales (**fmtid \_ MedicalInfo**).

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

N’oubliez pas que le CLSID de l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et les deux jeux de propriétés sont **CLSID \_ AnimalApp**. Cela identifie toute application qui peut afficher et/ou fournir un accès par programme à ces jeux de propriétés. Toute application peut lire les données dans les jeux de propriétés (le point derrière les jeux de propriétés), mais seules les applications identifiées avec l’identificateur de classe du CLSID \_ AnimalApp peuvent comprendre la signification des données dans les jeux de propriétés.

 

 




