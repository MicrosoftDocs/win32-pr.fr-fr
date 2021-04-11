---
title: Prise en charge de la liaison précoce
description: L’exemple de code suivant présente un scénario avec une prise en charge de la liaison précoce en place.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- ADSI d’extensions, prise en charge de la liaison précoce
- liaison AD, prise en charge de la liaison précoce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102340"
---
# <a name="early-binding-support"></a>Prise en charge de la liaison précoce

L’exemple de code suivant présente un scénario avec une prise en charge de la liaison précoce en place.


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



Dans cet exemple de code, deux composants d’extension étendent un objet **utilisateur** . Chaque extension publie sa propre interface. Chaque extension ne reconnaît pas l’autre interface d’extension ; seul ADSI reconnaît l’existence des deux extensions. Chaque extension délègue son [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) à ADSI. ADSI agit comme un agrégateur pour les deux extensions et toute autre extension future. L’interrogation d’une interface à partir de n’importe quelle extension, ou à partir d’ADSI, produit le même résultat cohérent.

La procédure suivante décrit comment créer une extension.

## <a name="step-1-add-aggregation-to-your-component"></a>Étape 1 : ajouter une agrégation à votre composant

Suivez la spécification COM pour ajouter une agrégation à votre composant. En résumé, vous devez accepter les demandes *pUnknown* à votre composant pendant **CreateInstance** et déléguer le *pUnknown* à l' [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’agrégateur si le composant est agrégé.

## <a name="step-2-register-your-extension"></a>Étape 2 : inscrire votre extension

Vous devez maintenant choisir la classe de répertoire à étendre. Vous ne pouvez pas utiliser les mêmes interfaces pour accomplir cela que vous utiliseriez pour une interface ADSI, par exemple [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer). Les objets d’annuaire sont conservés dans l’annuaire, tandis que votre extension et ADSI s’exécutent sur l’ordinateur client. Les exemples d’objets d’annuaire sont **User**, **Computer**, **PrintQueue**, **serviceConnectionPoint** et **nTDSService**. Vous pouvez ajouter une nouvelle classe dans Active Directory et créer également une nouvelle extension pour cette nouvelle classe.

Vous utilisez des clés de Registre pour associer un nom de classe d’annuaire à des composants d’extension ADSI. La figure suivante représente la disposition de Registre existante, ainsi que de nouvelles clés.

-   Une nouvelle clé, appelée **Extensions**, contient une liste de clés, chacune représentant une classe dans l’annuaire. Chaque classe, par exemple, **utilisateur**, **PrintQueue** ou **ordinateur**, gère une liste de sous-clés.
-   Chaque sous-clé contient le CLSID du composant d’extension ADSI.
-   Chaque sous-clé CLSID contient une entrée de chaîne qui autorise plusieurs valeurs. Vous devez uniquement répertorier les interfaces qui participent à l’agrégation.

> [!Note]  
> Les objets d’extension sont toujours requis pour enregistrer les clés COM standard.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a>Exemple

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

La liste des interfaces de Extension1 peut être différente de celle de extension2. L’objet, lorsqu’il est actif, prend en charge les interfaces de l’agrégateur (ADSI) et toutes les interfaces fournies par les Extension1 et extension2 de l’agrégat. La résolution des interfaces en conflit (la même interface que celle prise en charge par l’agrégateur et les agrégats ou par plusieurs agrégats) est déterminée par les priorités des extensions.

Vous pouvez également associer votre extension CLSID à plusieurs noms de classes d’objets. Par exemple, votre extension peut étendre à la fois les objets **utilisateur** et **contact** .

> [!Note]  
> Le comportement d’extension est ajouté sur une classe par objet, et non sur une instance par objet.

 

Il est recommandé d’inscrire vos extensions, comme vous le feriez pour tout autre composant COM, avec un appel à la fonction **DllRegisterSvr** . Fournissez également une fonctionnalité pour annuler l’inscription de votre extension avec la fonction **DllUnregisterServer** .

L’exemple de code suivant montre comment inscrire une extension.


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 