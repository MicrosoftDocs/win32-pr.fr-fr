---
description: Vous pouvez masquer le bouton Annuler qui est utilisé pour annuler une installation à l’aide d’une option de ligne de commande, de l’API Windows Installer ou d’une action personnalisée. Le bouton Annuler peut être masqué pour tout ou partie de l’installation, en fonction de la méthode que vous utilisez.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Masquage du bouton Annuler pendant une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529282"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a>Masquage du bouton Annuler pendant une installation

Vous pouvez masquer le bouton **Annuler** qui est utilisé pour annuler une installation à l’aide d’une option de ligne de commande, de l’API Windows Installer ou d’une action personnalisée. Le bouton **Annuler** peut être masqué pour tout ou partie de l’installation, en fonction de la méthode que vous utilisez.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Masquage du bouton Annuler à partir de la ligne de commande

Le bouton **Annuler** peut être masqué lors de l’installation à l’aide de l’option de ligne de commande ( !). Cette opération ne peut être effectuée que pour une installation de base au niveau de l’interface utilisateur (/QB). Le bouton **Annuler** est masqué pour l’ensemble de l’installation. Pour plus d’informations, consultez [options de ligne de commande](command-line-options.md) et niveaux d' [interface utilisateur](user-interface-levels.md). La ligne de commande suivante masque le bouton **Annuler** et installe Example.msi.

**msiexec/I example.msi/QB !**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Masquage du bouton Annuler d’une application ou d’un script

Vous pouvez écrire une application ou un script pour masquer le bouton **Annuler** . Cette opération ne peut être effectuée que pour une installation de base au niveau de l’interface utilisateur, de sorte que le bouton **Annuler** est masqué pour l’ensemble de l’installation.

Pour masquer le bouton Annuler d’une application, définissez INSTALLUILEVEL \_ HIDECANCEL lors de l’appel de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). L’exemple suivant masque le bouton **Annuler** et installe Example.msi.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



Pour masquer le bouton **Annuler** du script, ajoutez msiUILevelHideCancel à la propriété [**UILevel**](installer-uilevel.md) de l' [**objet installer**](installer-object.md). L’exemple VBScript suivant masque le bouton **Annuler** et installe Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Masquage du bouton Annuler pour les parties d’une installation à l’aide d’une action personnalisée

Votre installation peut masquer et afficher le bouton **Annuler** pendant les parties d’une installation en envoyant un \_ message INSTALLMESSAGE COMMONDATA à l’aide d’un script ou d’une action personnalisée dll. Pour plus d’informations, consultez [bibliothèques de liens dynamiques](dynamic-link-libraries.md), [scripts](scripts.md), [actions personnalisées](custom-actions.md)et [envoi de messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Un appel à une action personnalisée doit fournir un enregistrement. Le champ 1 de cet enregistrement doit contenir la valeur 2 (deux) pour spécifier le bouton **Annuler** . Le champ 2 doit contenir la valeur 0 ou 1. La valeur 0 dans le champ 2 masque le bouton et la valeur 1 dans le champ 2 affiche le bouton. Notez que l’allocation d’un enregistrement de taille 2 avec [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fournit les champs 0, 1 et 2.

L’exemple d’action personnalisée de DLL suivant masque le bouton **Annuler** .


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



L’action personnalisée VBScript suivante masque le bouton **Annuler** .


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



