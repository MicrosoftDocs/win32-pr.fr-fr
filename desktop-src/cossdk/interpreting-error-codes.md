---
description: Interprétation des codes d’erreur
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: Interprétation des codes d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659ee7def9feff50d375a07ab201e1cca25bffd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311030"
---
# <a name="interpreting-error-codes"></a>Interprétation des codes d’erreur

Une fois que vous avez déterminé quelle application est la source d’un problème, vous devez identifier l’erreur qui s’est produite. Les erreurs sont générées et signalées dans différents formats, selon le langage utilisé par votre application.

dans Microsoft Visual C++, les valeurs de réussite, d’avertissement et d’échec sont retournées à l’aide d’un nombre 32 bits connu sous le nom de **HRESULT**. pour obtenir la liste des valeurs **HRESULT** définies par le système, consultez le fichier d’en-tête Winerror. h inclus dans le SDK Windows. Ce fichier comprend tous les codes d’erreur et descriptions COM+. Pour plus d’informations sur les valeurs **HRESULT** , consultez [gestion des erreurs](/windows/desktop/com/error-handling-in-com).

En langage Java, une instance de com. ms. com. ComFailException est levée pour indiquer un échec, où l’objet ComFailException spécifie un **HRESULT**. Une instance de com. ms. com. ComSuccessException indique la réussite avec une valeur de retour false. Pour plus d’informations sur l’interprétation de ces exceptions, consultez la documentation de Microsoft Visual J++.

> [!Note]  
> Les processus de serveur d’applications COM+ qui hébergent des objets Visual J++ ne sont pas inactifs (même avec zéro objet actif), sauf si vous désactivez le débogage juste-à-temps dans l’IDE VJ6. Pour plus d’informations sur la façon de procéder, consultez la documentation de Visual J++.

 

dans Visual Basic, vous pouvez récupérer des valeurs **HRESULT** en examinant la propriété Err. Number. Une description de l’erreur peut être récupérée à l’aide de la propriété Err. Description.

vous pouvez également utiliser l’utilitaire ERRLOOK dans Microsoft Visual Studio pour récupérer un message d’erreur système ou un message d’erreur de module. ERRLOOK récupère le texte du message d’erreur automatiquement si vous glissez-déplacez une valeur hexadécimale ou décimale à partir du débogueur Visual Studio ou d’une autre application Automation. Vous pouvez également entrer une valeur en la tapant ou en la collant à partir du presse-papiers IDE et en cliquant sur l’option **Rechercher** .

La méthode C++ suivante imprime une description de l’erreur, en fonction de l’entrée **HRESULT**.


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>

void ErrorDescription(HRESULT hr) 
{ 
     if(FACILITY_WINDOWS == HRESULT_FACILITY(hr)) 
         hr = HRESULT_CODE(hr); 
     TCHAR* szErrMsg; 

     if(FormatMessage( 
       FORMAT_MESSAGE_ALLOCATE_BUFFER|FORMAT_MESSAGE_FROM_SYSTEM, 
       NULL, hr, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
       (LPTSTR)&szErrMsg, 0, NULL) != 0) 
     { 
         _tprintf(TEXT("%s"), szErrMsg); 
         LocalFree(szErrMsg); 
     } else 
         _tprintf( TEXT("[Could not find a description for error # %#x.]\n"), hr); 
}
```



Le tableau suivant fournit une description des codes d’erreur courants dans COM+.



| Codes d’erreur                                                   | Définitions                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALREADYINSTALLED comadmin \_ E \_<br/>                      | L’objet est déjà inscrit.<br/>                                                                                                                                                                     |
| fichier d' \_ application comadmin E \_ \_ \_ READFAIL<br/>                   | Une erreur s’est produite lors de la lecture du fichier d’application.<br/>                                                                                                                                                          |
| VERSION du \_ \_ fichier d' \_ application \_ comadmin E<br/>                    | Numéro de version non valide dans le fichier d’application.<br/>                                                                                                                                                           |
| fichier d' \_ application comadmin E \_ \_ \_ WRITEFAIL<br/>                  | Une erreur s’est produite lors de l’écriture dans le fichier d’application.<br/>                                                                                                                                                       |
| APPDIRNOTFOUND comadmin \_ E \_<br/>                        | Le répertoire d’installation de l’application est introuvable.<br/>                                                                                                                                                          |
| \_application COMQC E non mise en \_ \_ \_ file d’attente<br/>                 | Seules les applications COM+ marquées « en file d’attente » peuvent être créées à l’aide du moniker « file d’attente ».<br/>                                                                                                                      |
| APPLICATIONEXISTS comadmin \_ E \_<br/>                     | L’application est déjà installée.<br/>                                                                                                                                                                 |
| comadmin \_ E \_ applisd \_ correspond à \_ CLSID<br/>                | Un CLSID avec le même GUID que le nouvel ID d’application est déjà installé sur cet ordinateur.<br/>                                                                                                            |
| \_application comadmin \_ E \_ non \_ exécutée<br/>                     | L’application spécifiée n’est pas en cours d’exécution.<br/>                                                                                                                                                   |
| AUTHENTICATIONLEVEL comadmin \_ E \_<br/>                   | Impossible de définir le niveau d’authentification requis pour la demande de mise à jour.<br/>                                                                                                                                       |
| BADPATH comadmin \_ E \_<br/>                               | Le chemin d’accès au fichier n’est pas valide.<br/>                                                                                                                                                                             |
| BADREGISTRYLIBID comadmin \_ E \_<br/>                      | L’ID de bibliothèque de types inscrit n’est pas valide.<br/>                                                                                                                                                            |
| BADREGISTRYPROGID comadmin \_ E \_<br/>                     | Le ProgID du composant est manquant ou endommagé.<br/>                                                                                                                                                         |
| comadmin \_ E \_ \_ ne peut pas \_ Exporter le \_ proxy d’application \_<br/>          | Le proxy d’application n’est pas exportable.<br/>                                                                                                                                                              |
| comadmin \_ E \_ \_ ne peut pas \_ Démarrer l' \_ application<br/>                  | Échec du démarrage de l’application, car il s’agit d’une application de bibliothèque ou d’un proxy d’application.<br/>                                                                                                       |
| comadmin \_ E \_ \_ ne peut pas \_ exporter l' \_ \_ application sys<br/>            | L’application système ne peut pas être exportée.<br/>                                                                                                                                                             |
| comadmin \_ E ne pas \_ \_ s’abonner \_ au \_ composant<br/>        | L’utilisateur ne peut pas s’abonner à ce composant car le composant a peut-être été importé.<br/>                                                                                                             |
| CANTCOPYFILE comadmin \_ E \_<br/>                          | Une erreur s’est produite lors de la copie du fichier.<br/>                                                                                                                                                                   |
| CLSIDORIIDMISMATCH comadmin \_ E \_<br/>                    | Les CLSID ou IID du fichier d’application ne correspondent pas aux DLL correspondantes.<br/>                                                                                                                                      |
| comadmin \_ E \_ COMP \_ déplacer le \_ mauvais \_ dest.<br/>                 | Le déplacement du composant a échoué car l’application de destination n’existe plus.<br/>                                                                                                                       |
| migration de comadmin \_ E \_ COMP \_ \_ verrouillée<br/>                    | Le déplacement du composant a été interdit, car l’application source ou de destination est une application système ou est actuellement verrouillée contre les modifications.<br/>                                                |
| comadmin \_ E \_ COMPFILE \_ BADTLB<br/>                      | Impossible de charger la bibliothèque de types.<br/>                                                                                                                                                                 |
| comadmin \_ E \_ COMPFILE \_ CLASSNOTAVAIL<br/>               | La DLL ne prend pas en charge les composants listés dans la bibliothèque de types.<br/>                                                                                                                                   |
| comadmin \_ E \_ COMPFILE \_ DOESNOTEXIST<br/>                | Ce fichier n’existe pas.<br/>                                                                                                                                                                             |
| comadmin \_ E \_ COMPFILE \_ GETCLASSOBJ<br/>                 | La méthode [**GetClassObject,**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) a échoué dans la dll.<br/>                                                                                                                |
| comadmin \_ E \_ COMPFILE \_ LOADDLLFAIL<br/>                 | La DLL n’a pas pu être chargée.<br/>                                                                                                                                                                          |
| \_ \_ COMPFILE \_ noregistrar<br/>                 | Le Bureau d’enregistrement de composants référencé dans ce fichier n’est pas disponible.<br/>                                                                                                                                     |
| comadmin \_ E \_ COMPFILE \_ NOTINSTALLABLE<br/>              | Le fichier ne contient pas d’informations sur les composants ou les composants.<br/>                                                                                                                                        |
| COREQCOMPINSTALLED comadmin \_ E \_<br/>                    | Un composant de la même DLL est déjà installé.<br/>                                                                                                                                                     |
| DLLLOADFAILED comadmin \_ E \_<br/>                         | La DLL n’a pas pu être chargée.<br/>                                                                                                                                                                          |
| comadmin \_ E \_ DLLREGISTERSERVER<br/>                     | La fonction [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) a échoué lors de l’installation du composant.<br/>                                                                                                  |
| EVENTCLASS de comadmin \_ E \_ \_ \_ ne peut pas être \_ abonné<br/>      | Une classe d’événements ne peut pas être configurée en tant que composant d’abonné. En cas de tentative de création d’un abonnement avec une classe d’événements en tant qu’abonné, cette erreur est retournée.<br/>                          |
| INVALIDUSERIDS comadmin \_ E \_<br/>                        | Un ou plusieurs utilisateurs dans le fichier d’application ne sont pas valides.<br/>                                                                                                                                              |
| MANQUE de keyadmin \_ E \_<br/>                            | L’objet est introuvable dans le catalogue.<br/>                                                                                                                                                              |
| le proxy d’application comadmin \_ E \_ lib est \_ \_ \_ incompatible<br/>         | Les applications de bibliothèque et les proxys d’application ne sont pas compatibles. Cette erreur est retournée lorsqu’une tentative d’exportation d’un proxy d’application est effectuée et que la propriété d’activation de l’application est une bibliothèque. <br/> |
| NOREGISTRYCLSID comadmin \_ E \_<br/>                       | Le CLSID du composant est manquant ou endommagé.<br/>                                                                                                                                                          |
| NOSERVERSHARE comadmin \_ E \_<br/>                         | Aucun partage de fichiers serveur n’est disponible.<br/>                                                                                                                                                                    |
| NOTCHANGEABLE comadmin \_ E \_<br/>                         | Les modifications apportées à cet objet et à ses sous-objets ont été désactivées.<br/>                                                                                                                                        |
| NOTDELETEABLE comadmin \_ E \_<br/>                         | La fonction Delete a été désactivée pour cet objet.<br/>                                                                                                                                                |
| NOTINREGISTRY comadmin \_ E \_<br/>                         | L’objet est introuvable dans le registre.<br/>                                                                                                                                                                     |
| comadmin \_ E \_ nouser<br/>                                | Un ou plusieurs utilisateurs ne sont pas valides.<br/>                                                                                                                                                                      |
| l’objet comadmin \_ E \_ \_ n' \_ \_ existe pas<br/>              | L’un des objets spécifiés est introuvable.<br/>                                                                                                                                                         |
| le parent de l’objet comadmin \_ E est \_ \_ \_ manquant<br/>               | L’un des objets insérés ou mis à jour n’appartient pas à une collection parent valide.<br/>                                                                                                            |
| OBJECTERRORS comadmin \_ E \_<br/>                          | Des erreurs se sont produites lors de l’accès à un ou plusieurs objets. Pour plus d’informations, consultez la collection [**errorInfo**](errorinfo.md) .<br/>                                                                               |
| OBJECTEXISTS comadmin \_ E \_<br/>                          | L’objet que vous tentez d’ajouter ou de renommer existe déjà.<br/>                                                                                                                                        |
| OBJECTINVALID comadmin \_ E \_<br/>                         | Une ou plusieurs des propriétés de l’objet sont manquantes ou non valides.<br/>                                                                                                                                        |
| OBJECTNOTPOOLABLE comadmin \_ E \_<br/>                     | Cet objet ne peut pas être regroupé.<br/>                                                                                                                                                                      |
| PROPERTYSAVEFAILED comadmin \_ E \_<br/>                    | Un ou plusieurs paramètres de propriété ne sont pas valides ou sont en conflit l’un avec l’autre.<br/>                                                                                                                      |
| débordement de la propriété comadmin \_ E \_ \_<br/>                    | La valeur de la propriété est trop grande.<br/>                                                                                                                                                                      |
| comadmin \_ E \_ REGFILE \_ endommagé<br/>                      | Le fichier d’inscription est endommagé.<br/>                                                                                                                                                                     |
| REGISTERTLB comadmin \_ E \_<br/>                           | Le système n’a pas pu inscrire la bibliothèque de types.<br/>                                                                                                                                                   |
| REGISTRARFAILED comadmin \_ E \_<br/>                       | Des erreurs se sont produites lors de l’inscription du composant.<br/>                                                                                                                                                     |
| REMOTEINTERFACE comadmin \_ E \_<br/>                       | Les informations de l’interface sont manquantes ou modifiées.<br/>                                                                                                                                                   |
| comadmin \_ E \_ requiert \_ une \_ plateforme différente<br/>         | Cette opération n’est pas activée sur cette plateforme.<br/>                                                                                                                                                       |
| le rôle comadmin \_ E \_ \_ n' \_ \_ existe pas<br/>                | Un rôle affecté à un composant, une interface ou une méthode n’existe pas dans l’application.<br/>                                                                                                               |
| ROLEEXISTS comadmin \_ E \_<br/>                            | Le rôle existe déjà.<br/>                                                                                                                                                                              |
| SERVICENOTINSTALLED comadmin \_ E \_<br/>                   | Le service n’est pas installé.<br/>                                                                                                                                                                         |
| SESSION comadmin \_ E \_<br/>                               | La version du catalogue du serveur n’est pas prise en charge.<br/>                                                                                                                                                          |
| comadmin \_ S \_ SOMEALREADYPAUSED<br/>                     | Un ou plusieurs des processus d’application spécifiés ont déjà été suspendus.<br/>                                                                                                                               |
| comadmin \_ S \_ SOMEALREADYRUNNING<br/>                    | Un ou plusieurs des processus d’application spécifiés étaient déjà en cours d’exécution.<br/>                                                                                                                              |
| comadmin \_ E \_ Start \_ application \_ Needs \_ Components<br/>         | Pour démarrer l’application, vous devez disposer de composants dans une application.<br/>                                                                                                                                 |
| \_SVCAPP de comadmin E \_ \_ non \_ regroupable \_ ou \_ recyclable<br/> | Les applications COM+ s’exécutant en tant que service NT peuvent ne pas être marquées comme étant regroupées ou recyclées.<br/>                                                                                                               |
| SYSTEMAPP comadmin \_ E \_<br/>                             | Cette opération ne peut pas être effectuée sur l’application système.<br/>                                                                                                                                         |
| \_utilisateur comadmin \_ E \_ dans \_ Set<br/>                         | Un ou plusieurs utilisateurs sont déjà affectés à un ensemble de partitions local.<br/>                                                                                                                                      |
| USERPASSWDNOTVALID comadmin \_ E \_<br/>                    | L’identité ou le mot de passe défini sur l’application n’est pas valide.<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Isolation des erreurs et stratégie FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Recherche de la source d’une erreur](finding-the-source-of-an-error.md)
</dt> <dt>

[Modification des valeurs de retour par COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Stratégies de gestion des erreurs dans COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Dépannage](troubleshooting-the-com--crm.md)
</dt> </dl>

 

