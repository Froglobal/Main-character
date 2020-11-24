# Main-character
操作するキャラにインポートして使います

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class MainCharacter : MonoBehaviour
{
    void Update()
    {
        /*オブジェクトの座標を取得します*/
        Quaternion quaternion = this.transform.rotation;
        Debug.Log(quaternion);
        float y = quaternion.eulerAngles.y;

        //前に移動します
        if (Input.GetKey(KeyCode.W))
        {
            //316°～ 45°の角度の時に進む方向
            if (316 <= y && y <= 360 || y <= 45)
            {
                transform.position += new Vector3(0, 0, 6 * Time.deltaTime);
            }

            //46°～ 135°の角度の時に進む方向
            else if (46 <= y && y <= 135)
            {
                transform.position += new Vector3(6 * Time.deltaTime, 0, 0);
            }

            //136°～ 225°の角度の時に進む方向
            else if (136 <= y && y <= 225)
            {
                transform.position += new Vector3(0, 0, -6 * Time.deltaTime);
            }

            //226°～ 315°の角度の時に進む方向
            else if (226 <= y && y <= 315)
            {
                transform.position += new Vector3(-6 * Time.deltaTime, 0, 0);
            }
        }

        //後に移動します
        if (Input.GetKey(KeyCode.X))
        {
            //316°～ 45°の角度の時に進む方向
            if (316 <= y && y <= 360 || y <= 45)
            {
                transform.position += new Vector3(0, 0, -6 * Time.deltaTime);
            }

            //46°～ 135°の角度の時に進む方向
            else if (46 <= y && y <= 135)
            {
                transform.position += new Vector3(-6 * Time.deltaTime, 0, 0);
            }

            //136°～ 225°の角度の時に進む方向
            else if (136 <= y && y <= 225)
            {
                transform.position += new Vector3(0, 0, 6 * Time.deltaTime);
            }

            //226°～ 315°の角度の時に進む方向
            else if (226 <= y && y <= 315)
            {
                transform.position += new Vector3(6 * Time.deltaTime, 0, 0);
            }
        }

        //右に移動します
        if (Input.GetKey(KeyCode.D))
        {
            //316°～ 45°の角度の時に進む方向
            if (316 <= y && y <= 360 || y <= 45)
            {
                transform.position += new Vector3(6 * Time.deltaTime, 0, 0);
            }

            //46°～ 135°の角度の時に進む方向
            else if (46 <= y && y <= 135)
            {
                transform.position += new Vector3(0, 0, -6 * Time.deltaTime);
            }

            //136°～ 225°の角度の時に進む方向
            else if (136 <= y && y <= 225)
            {
                transform.position += new Vector3(-6 * Time.deltaTime, 0, 0);
            }

            //226°～ 315°の角度の時に進む方向
            else if (226 <= y && y <= 315)
            {
                transform.position += new Vector3(0, 0, 6 * Time.deltaTime);
            }
        }

        //左に移動します
        if (Input.GetKey(KeyCode.A))
        {
            //316°～ 45°の角度の時に進む方向
            if (316 <= y && y <= 360 || y <= 45)
            {
                transform.position += new Vector3(-6 * Time.deltaTime, 0, 0);
            }

            //46°～ 135°の角度の時に進む方向
            else if (46 <= y && y <= 135)
            {
                transform.position += new Vector3(0, 0, 6 * Time.deltaTime);
            }

            //136°～ 225°の角度の時に進む方向
            else if (136 <= y && y <= 225)
            {
                transform.position += new Vector3(6 * Time.deltaTime, 0, 0);
            }

            //226°～ 315°の角度の時に進む方向
            else if (226 <= y && y <= 315)
            {
                transform.position += new Vector3(0, 0, -6 * Time.deltaTime);
            }
        }
    }
}
